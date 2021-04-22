<template>
  <div class="Section">
    <HeaderWithButton @OpenClose="OC = !OC" :title="Title" :bText="BText" :bColor="BColor" onClickEvent="OpenClose" />
    <p v-if="OC">
      {{ Text }}
    </p>
  </div>
</template>

<script>
import HeaderWithButton from './HeaderWithButton'

export default {
  name: 'SectionWithOCButton',
  props: {
    Title: {
      type: String,
      required: true
    },
    Text: {
      type: String,
      required: true
    },
    BText: {
      type: String,
      required: true
    },
    BColor: {
      type: String,
      required: true
    }
  },
  components: {
    HeaderWithButton
  },
  data() {
    return {
      OC = true
    }
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