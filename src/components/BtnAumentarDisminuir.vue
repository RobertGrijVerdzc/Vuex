<template>
  <button>{{ textoBoton }}</button>
</template>

<script>
import {mapActions} from 'vuex'
export default {
    props:{
        estado : Boolean
    },
    data() {
        return {
            
        }
    },
    computed:{
        textoBoton(){
            return this.estado ? 'Aumentar' : 'Disminuir'
        }
    },
    methods: {
        
    },
}
</script>