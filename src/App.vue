<script setup>
import { ref } from 'vue'

const inputText = ref('')
const tempText = ref('')

const enterInputValue = (e) => {
  if(tempText.value.length <= 10) {
    inputText.value = tempText.value
  } 
  
}

</script>

<template>
<div>
    <h2>
      Enter name:
    </h2>
    <input v-model="tempText" type="text" @keyup="enterInputValue($event)"/>
    <p>
      Entered name: {{ inputText }}
    </p>
</div>
</template>

<style scoped>
</style>
