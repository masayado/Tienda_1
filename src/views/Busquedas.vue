<template>
    <div>
        <div class="busqueda">
            <h1> Busca tu juego</h1>
            <input type="text" placeholder="Ingresa codigo">
            <hr>
                <p>Cantidad de juegos disponibles: {{totalJuegos}}</p>
            <hr>
        </div>
        <div class="lista_juegos">
        <lista-juegos></lista-juegos>
        </div>
    </div>
</template>

<script>
import Lista from '@/components/Lista.vue'
import {mapState, mapGetters} from 'vuex';
export default {
    name: 'busquedas',
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
        ...mapState(['juegos']),
        ...mapGetters(['totalJuegos']),
    //...mapState({
    //    juegos:(state)=>state.juegos
    //}),
    },
    methods: {
        
    },
    components: {
        'lista-juegos':Lista,
    },
}
</script>

<style scoped>
.busqueda{
    text-align:center;
}

.busqueda input{
    margin-bottom:15px;
}

.lista_juegos{
    display:flex;
    justify-content: center;
}
</style>