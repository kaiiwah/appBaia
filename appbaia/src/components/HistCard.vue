<template>
    <div class="text-h7">
      <p v-for = "texto in historia.texto" v-bind:key="texto">
        {{ texto }}
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
