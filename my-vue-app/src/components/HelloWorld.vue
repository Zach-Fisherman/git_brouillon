<template>
  <div>
    <span v-if="bool">{{message}}</span>
    <span v-if="!bool">{{tableau}}</span>
    <button @click="changerBool">Changer d'affichage</button>
  </div>
  <input-Exo/>
</template>

<script lang="ts">
import { ref, defineComponent } from 'vue'
import inputExo from './input.vue'
import texteExo from './texte.vue'
import listeExo from './texte.vue'

export default defineComponent({
  name: 'Donnees',
  data(){
  return{
    message: 'Mon message',
    bool: true,
    tableau: ['Clavier','Souris','Trousse']
  }
  },
  methods: {
    changerBool(){
      this.bool = !this.bool;
    }
  },
  components : {
    inputExo, texteExo, listeExo,
  },
  setup: () => {
    const count = ref(0)
    return { count }
  }
})
</script>

<style scoped>
a {
  color: #00ff8c;
}
</style>