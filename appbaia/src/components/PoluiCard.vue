<template>
  <div class="text-h6">{{ historia.titulo2 }}</div>
    <div class="text-h7">
      <p v-for = "texto2 in historia.texto2" v-bind:key="texto2">
        {{ texto2 }}
      </p>
  </div>
</template>

<script>
export default {
props: {
  historia: {
    type: Object,
    required: false
  }
}
}

</script>
<style>

</style>
