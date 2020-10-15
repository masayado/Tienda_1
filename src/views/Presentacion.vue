<template>
<div>
   <div class="encabezado">
      <h1>32 Bits</h1>
      <h2>Juegos de PC y Consola</h2>
    </div>
    <nav class="menu">
      <ul>
        <li><router-link :to="{name: 'inicio'}">Inicio</router-link></li>
        <li><router-link :to="{name: 'busquedas'}">Búsquedas</router-link></li>
        <li><router-link :to="{name: 'ventas'}">Ventas</router-link></li>
        <li><router-link :to="{name: 'total'}">Total</router-link></li>
      </ul>
      <transition name="vista">
        <router-view></router-view>
      </transition>
    </nav>
</div>
</template>

<script>
export default {
    name: 'presentacion-component',
    // props: {},
    data: function(){
        return {}
    },
    // computed: {},
    methods: {
        // -- Metodos
    },
    //components: {},
}
</script>

<style scoped>
    
</style>