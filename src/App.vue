<template>
  <div id="app">
    <img alt="logo" src="./assets/logo.png">
    <presentacion-component></presentacion-component>
  </div>

  
</template>

<script>
import Presentacion from '@/views/Presentacion.vue'
export default {
  components:{
    'presentacion-component':Presentacion,
  },
}
</script>

<style scoped>

body{
  padding:0;
  margin:0;
  box-sizing:border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
.vista-enter-active, .vista-leave-active {
    transition: opacity .1s;
}
.vista-enter, .vista-leave-to{
    opacity: 0;
}

</style>