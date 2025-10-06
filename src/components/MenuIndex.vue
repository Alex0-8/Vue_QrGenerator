<template>
    <section>
        <div class="menu-header">
            <h2>Menú</h2>
            <button><i><svg viewBox="0 0 24 24" width="24" height="24" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round" class="css-i6dzq1"><line x1="18" y1="6" x2="6" y2="18"></line><line x1="6" y1="6" x2="18" y2="18"></line></svg></i></button>
        </div>        
    </section>
</template>

<script>
    export default {
        name: "MenuIndex",

    }
</script>

<style scoped>
    section{
        width: 40%;
        border-radius: 8px;
        padding: 15px;
    }

    .menu-header{
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
</style>