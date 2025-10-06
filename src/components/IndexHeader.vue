<template>
    <header class="header">
        <h1>{{ title }}</h1>

        <button><i><svg viewBox="0 0 24 24" width="24" height="24" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round" class="css-i6dzq1"><line x1="3" y1="12" x2="21" y2="12"></line><line x1="3" y1="6" x2="21" y2="6"></line><line x1="3" y1="18" x2="21" y2="18"></line></svg></i></button>
    </header>
</template>

<script>
    export default {
        name: "IndexHeader",
        props: {
            title: {
                type: String,
                default: "Texto a Qr"
            }
        } 
    }
</script>

<style scoped>
    header{
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 15px;
        background-color: #2c3e50;
        border-bottom: 2px solid #000;
        margin-bottom: 15px;
    }

    button{
        cursor: pointer;
        transition: all .3s ease;
        background-color: unset;
        border: none;
    }

    button:hover::after{
        transform: scale(.8);
    }

    button:hover{
        transform: scale(1.1);
    }
</style>