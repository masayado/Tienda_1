<template>
    <div>
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
    name: 'listajuegos-component',
    props: {
        juegos:{
            type:Array,
            required:true,
        },
    },
    data: function(){
        return {}
    },
    computed: {
        ...mapState(['juegos'])
    },
    methods: {
        // -- Metodos
    },
    //components: {},
}
</script>

<style scoped>

.lista{
    margin:0 auto;
}

    
</style>