<template>
  <div class="text-h7">
    <p v-for = "texto6 in historia.texto6" v-bind:key="texto6">
      {{ texto6 }}
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
