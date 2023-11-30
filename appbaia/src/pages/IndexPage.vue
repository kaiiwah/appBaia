<template>
  <q-page class = "fundomar">
    <div class = "titulo">
      <div class="text-h4">SOS Baia</div>

    </div>

      <div class = "card">
        <HistCard />
      </div>
      <div class = "card">
        <PoluiCard/>
      </div>
      <div class = "card">
        <PreserCard/>
      </div>
      <div class = "card">
        <CurioCard/>
      </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'
import HistCard from 'src/components/HistCard.vue';
import CurioCard from 'src/components/CurioCard.vue';
import PoluiCard from 'src/components/PoluiCard.vue';
import PreserCard from 'src/components/PreserCard.vue';

export default {
  components: {
    HistCard,
    CurioCard,
    PoluiCard,
    PreserCard
},
};
</script>

<style>
.fundomar {
  background-size: cover;
  background-image: url(../assets/Baia-de-todos-os-santos.webp);
  background-position: center;
  background-attachment: fixed;
}
.card{
  margin-bottom: 1px;
  flex-direction: column;
  display: flex;
  padding: 1em;
}
.titulo {
  padding: 0.5em;
}


</style>
