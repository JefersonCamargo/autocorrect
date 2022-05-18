<template>

  <input v-model="word"
         placeholder="Write a word">

</template>

<script>
export default {
  name: "InputAutocorrect",
  data() {
    return {
      word: '',
      words: {
        'correjir:': 'corregir',
        'correcion': 'corrección',
        'reevaluar': 'revaluar',
        'tezt': 'test',
      }
    }
  },
  watch: {
    word(value, oldValue) {
      if (value in this.words) {
        this.word = this.words[value]
      }
    }
  }

}
</script>

<style scoped>

</style>