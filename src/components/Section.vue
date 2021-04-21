<template>
  <div class="Section">
    <Header :title="Title" />
    <p>
      {{ Text }}
    </p>
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
div.Section {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  flex-direction: column;
}
</style>