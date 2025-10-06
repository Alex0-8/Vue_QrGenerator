<template>
    <main>
        <section>
            <div class="qr-generator">
                <label for="txt">Escibe tu texto</label>
                <input v-model="text" type="txt" id="txt" placeholder="...">
                <canvas ref="canvas" ></canvas>
            </div>
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
    border-radius: 8px;
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

</style>