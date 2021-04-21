<template>
  <div>
    
  </div>
</template>

<script>
import Header from './Header'

export default {
  name: 'Section',
  props: {
    Title: {
      type: String,
      required: true
    },
    Text: {
      type: String,
      required: true
    }
  },
  components: {
    Header
  }
}
</script>

<style scoped>
div {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>