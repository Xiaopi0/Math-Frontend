<template>
  <div class="Section">
    <HeaderWithButton :title="Title" :bText="BText" :bColor="BColor" :onClickEvent="OnClickEvent" />
    <p>
      {{ Text }}
    </p>
  </div>
</template>

<script>
import HeaderWithButton from './HeaderWithButton'

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
    },
    BText: {
      type: String,
      required: true
    },
    BColor: {
      type: String,
      required: true
    },
    OnClickEvent: {
      type: String,
      required: true
    }
  },
  components: {
    HeaderWithButton
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