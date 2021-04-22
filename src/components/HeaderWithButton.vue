<template>
  <header class="Header">
    <h1>{{ title }}</h1>
    <Button @OpenClose="$emit('OpenClose')" :text="bText" :color="bColor" :onclickEvent="onClickEvent" />
  </header>
</template>

<script>
import Button from './Button'
export default {
  name: 'HeaderWithButton',
  props: {
    title: {
      type: String,
      required: true,
    },
    bColor: {
      type: String,
      required: true
    },
    bText: {
      type: String,
      required: true
    },
    onClickEvent: {
      type: String,
      required: true
    }
  },
  components: {
    Button,
  },
}
</script>

<style scoped>
header.Header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-direction: row;
  margin-bottom: 20px;
}
</style>