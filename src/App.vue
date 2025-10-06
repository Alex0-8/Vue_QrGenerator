<template>
  <IndexHeader title="Texto a Qr"/>
  <TextToQr />
</template>

<script>
import IndexHeader from './components/IndexHeader.vue';
import TextToQr from './components/TextToQr.vue';

export default {
  name: 'App',
  components: {
    IndexHeader,
    TextToQr
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #42b983;
}
</style>
