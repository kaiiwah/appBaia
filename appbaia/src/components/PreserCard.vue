<template>
  <div class="text-h7">
    <p v-for = "texto5 in historia.texto5" v-bind:key="texto5">
      {{ texto5 }}
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
