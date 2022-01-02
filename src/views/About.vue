<template>
  <h1>Pagina About V-Model</h1>
  <hr>
  <input type="{{ texto }}" v-model="texto">
  <h2>{{ texto }}</h2>
</template>

<script>
export default {
  data() {
    return {
      texto: ''
    }
  },
}
</script>

<style>

</style>