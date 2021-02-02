<template>
    <div>
        <input type="text" v-model="messageVide" />
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'input',
  data(){
    return{
        messageVide: '',
    }
  },
  components: {
  }
})
</script>