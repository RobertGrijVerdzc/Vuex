<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <h1
      :style="colorContador"
    >El contador es: {{ contador }}</h1>
  </div> 
  <button @click="accionIncrementar()">Incrementar</button>
  <DisminuirBtn/>
  <hr>
  <BtnAumenarDisminuir :estado="true"/>
  <BtnAumenarDisminuir :estado="false"/>
</template>

<script>
// @ is an alias to /src
import DisminuirBtn from '../components/BtnDisminuir.vue'
import BtnAumenarDisminuir from '../components/BtnAumentarDisminuir.vue'
import {mapState, mapMutations, mapActions} from 'vuex'
export default {
  name: 'Home',
  components: {
    DisminuirBtn,
    BtnAumenarDisminuir
  },
  computed:{
    ...mapState(['contador']),
    colorContador(){
      return [this.contador >= 100 ? {'color' : 'green'} : {'color': 'red'}]
    }
  },
  methods: {
    ...mapMutations(['incrementar']),
    ...mapActions(['accionIncrementar'])
  },
}
</script>
