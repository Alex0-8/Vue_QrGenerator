<template>
    <main>
        <section class="qr-generator">
                <label for="txt">Escibe tu texto</label>
                <div>
                    <button @click="cleanTxt"><svg viewBox="0 0 24 24" width="24" height="24" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round" class="css-i6dzq1"><polyline points="23 4 23 10 17 10"></polyline><polyline points="1 20 1 14 7 14"></polyline><path d="M3.51 9a9 9 0 0 1 14.85-3.36L23 10M1 14l4.64 4.36A9 9 0 0 0 20.49 15"></path></svg></button>
                    <input v-model="text" type="txt" id="txt" placeholder="...">
                    <button @click="pasteText" class="paste-txt">Pegar</button>
                </div>
                <canvas ref="canvas" ></canvas>
        </section>
    </main>
</template>

<script>
import QRCode from 'qrcode' // permite generear codigos qr desde desde java

export default {
    name: 'QrGenerator',
    data() {
        return {
            text: 'Texto de ejemplo'
        };
    },
    watch: { // cuando cambie text, ejecuta generateQR con el nuevo valor, cambiando el qr en tiempo real
        text(newValue){ 
            this.generateQR(newValue);
        },
    },
    mounted() { // se ejecuta cuando se monta el componente generando el qr inicial
        this.generateQR(this.text);
    },
    methods: {
        async generateQR(value) {
            try {
                await QRCode.toCanvas(this.$refs.canvas, value, { //accede directamente al canvas
                    width: 200,
                    color: {
                        dark: '#3cecd6',
                        light: "#30344a"
                    }
                })
            }catch (err) {
                console.log(`Ha ocurrido un error: ${err}`)
            }
        },

        cleanTxt() {
            this.text = "";
        },

        async pasteText() {
            try{
                const textFromClipboard = await navigator.clipboard.readText();
                if(textFromClipboard){
                    this.text = textFromClipboard;
                }else{
                    console.log("no se encontro nada en el portapapeles")
                }
            }catch(err){
                console.error("no se pudo acceder al portapapeles")
            }
        }
    }
}
</script>

<style scoped>

.qr-generator {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 20px;
}

label{
    font-size: 26px;
}

input{
    font-size: 20px;
    padding: 5px;
    background-color: #212433;
    outline: none;
    color: #fff;
    border: 2px solid #0075f300;
    transition: all .2s linear;
}

input:focus{
    border: 2px solid #c92ff8;
}

div{
    display: flex;
    justify-items: center;

    button {
        cursor: pointer;
        padding: 5px;
        background-color: #24f3db;
        border-radius: 8px 0 0 8px;
        border: none;
        transition: all .3s ease;

        &:hover{
            transform: scale(1.05);
        }

        &:active{
            transform: scale(.9);
        }
    }

    .paste-txt{
        border-radius: 0 8px 8px 0;
    }
}

</style>