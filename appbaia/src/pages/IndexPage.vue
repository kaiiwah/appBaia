<template>
  <div class = "fundomar">
    <div class = "estilo">

      <h4 center class="titulo">HISTÓRIA DA BAÍA DE TODOS OS SANTOS</h4>
      <q-card-section horizontal>
        <q-card-section>
          <HistCard v-for="h in historias" v-bind:key="h" :historia='h'/>
        </q-card-section>
        <q-parallax src="https://www.brasil-turismo.com/imagens/baia-todos-santos.jpg"
        class="parallax-custom" >
        </q-parallax>
      </q-card-section>

      <h4 class="titulo">A POLUIÇÃO NA BAÍA DE TODOS OS SANTOS</h4>
      <q-card-section horizontal>
        <q-parallax src="https://museudoamanha.org.br/sites/default/files/01.jpg"
        class="parallax-custom2">
        </q-parallax>
        <q-card-section>
          <PoluiCard v-for="h in historias" v-bind:key="h" :historia='h'/>
        </q-card-section>
      </q-card-section>
      <q-card-section horizontal>
        <q-card-section>
          <PoluiCard2 v-for="h in historias" v-bind:key="h" :historia='h'/>
        </q-card-section>
        <q-parallax src="https://s2-g1.glbimg.com/69x7iV8tIJkUR8w02nQdPc7xf3s=/0x0:4155x2770/984x0/smart/filters:strip_icc()/i.s3.glbimg.com/v1/AUTH_59edd422c0c84a879bd37670ae4f538a/internal_photos/bs/2019/p/e/lPCmapRwGtX6KXNMCl3w/2019-10-12t135111z-2127616760-rc1d32278e00-rtrmadp-3-brazil-environment-oil.jpg"
        class="parallax-custom3">
        </q-parallax>
      </q-card-section>
      <q-card-section horizontal>
        <q-parallax src="https://s.glbimg.com/jo/g1/f/original/2014/10/27/baia_7.jpg"
        class="parallax-custom4">
        </q-parallax>
        <q-card-section>
          <PoluiCard3 v-for="h in historias" v-bind:key="h" :historia='h'/>
        </q-card-section>
      </q-card-section>

      <h4 center class="titulo">COMO PRESERVAR O AMBIENTE MARINHO</h4>
      <q-card-section horizontal>
        <q-card-section>
          <PreserCard v-for="h in historias" v-bind:key="h" :historia='h'/>
        </q-card-section>
        <q-parallax src="https://static.wixstatic.com/media/2f8685_f92f23b48386406782f8281809b912fa~mv2.jpg/v1/fit/w_1000%2Ch_673%2Cal_c%2Cq_80,enc_auto/file.jpg"
        class="parallax-custom5" >
        </q-parallax>
      </q-card-section>

      <h4 class="titulo">CURIOSIDADES SOBRE A BAÍA DE TODOS OS SANTOS</h4>
      <q-card-section horizontal>
        <q-parallax src="https://i2.wp.com/ciencianarua.net/wp-content/uploads/2019/10/Vista_da_Baia_de_Todos_os_Santos-copy.jpg?fit=999%2C700&ssl=1"
        class="parallax-custom">
        </q-parallax>
        <q-card-section>
          <CurioCard v-for="h in historias" v-bind:key="h" :historia='h'/>
        </q-card-section>
      </q-card-section>
    </div>
  </div>
</template>

<script>
import { defineComponent } from 'vue'
import axios from 'src/boot/axios';
import HistCard from 'src/components/HistCard.vue';
import PoluiCard from 'src/components/PoluiCard.vue';
import PoluiCard2 from 'src/components/PoluiCard2.vue';
import PoluiCard3 from 'src/components/PoluiCard3.vue';
import PreserCard from 'src/components/PreserCard.vue';
import CurioCard from 'src/components/CurioCard.vue';
import { Axios } from 'axios';

export default {
  components: {
    HistCard,
    PoluiCard,
    PoluiCard2,
    PoluiCard3,
    PreserCard,
    CurioCard
},
data(){
  return {
    historias: [ ]
  }
},
created(){
  const axios = require('axios');

  axios.get("http://localhost:3000/historia").then((resposta)=>{
    console.log(resposta.data)
    this.historias=resposta.data
  })
}
};

</script>

<style>
.fundomar {
  background-size: cover;
  background-image: url(../assets/Baia-de-todos-os-santos.webp);
  background-position: center;
  background-attachment: fixed;
  padding: 20px;

}

.titulo {
  text-align :center;
  margin: 20px;
  margin-bottom: 30px;
  padding-top: 20px;
}

.parallax-custom {
  size: cover;
  width: 130%;
  height: 50%;
  max-height: auto;
}

.parallax-custom2 {
  width: 250%;
  max-height: auto;
}
.parallax-custom3 {
  width: 300%;
  size: cover;
  height: auto;
}

.parallax-custom4 {
  width: 199%;
}

.parallax-custom5 {
  width: 175%;
  max-height: auto;
}

.estilo {
  background-color: rgba(243, 245, 248, 0.9);
}
</style>
