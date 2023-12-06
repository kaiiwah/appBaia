<template>

  <div class="text-h6">{{ historia.titulo3 }}</div>
    <div class="text-h7">
      <p v-for = "texto3 in historia.texto3" v-bind:key="texto3">
        {{ texto3 }}
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
