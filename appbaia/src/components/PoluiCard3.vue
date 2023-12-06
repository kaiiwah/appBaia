<template>
  <div class="text-h6">{{ historia.titulo4 }}</div>
    <div class="text-h7">
      <p v-for = "texto4 in historia.texto4" v-bind:key="texto4">
        {{ texto4 }}
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
