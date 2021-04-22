<template>
  <button @click="$emit(onclickEvent)" :style="{ background: color }" class="btn">
    {{ text }}
  </button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    text: {
      type: String,
      required: true,
    },
    color: {
      type: String,
      required: true,
    },
    onclickEvent: {
      type: String,
      required: true
    }
  },
}
</script>