<template>
    <div>
        <div class="busqueda">
            <h1> Busca tu juego</h1>
            <input type="text" 
            placeholder="Ingresa codigo" 
            v-model="buscar" 
            @change="buscando">
            <hr>
            Cantidad de juegos disponibles: {{juegos_total}}
            <hr>
        </div>
        <div class="lista">
            <ul>
                <li v-for="juego in juegos" :key="juego.codigo">
                     <span class="lista_juegos" :style="{background: juego.color}">
                        {{juego.codigo}} |
                        {{juego.nombre}} |
                        {{juego.stock}} |
                        {{juego.precio}}
                    </span>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
import {mapState} from 'vuex';
export default {
    name: 'busquedas',
    props: {
        juegos:{
            type:Array,
            required:true,
        },
        juegos_total:{},
    },
    data: function(){
        return {}
    },
    computed: {
    //    ...mapState(['juegos'])
    ...mapState({
        juegos:(state)=>state.juegos
    })
    },
    methods: {
        
    },
    //components: {},
}
</script>

<style scoped>
.busqueda{
    text-align:center;
}

.busqueda input{
    margin-bottom:15px;
}
</style>