<template>
  <button class="text-red-700 bg-green-500" @click="clickAction(todo)">
    {{ title }}
  </button>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: {
    title: {
      type: String,
      default: '',
    },
    clickAction: {
      type: Function,
    },
    todo: {
      type: String,
      default: '',
    },
  },
})
</script>
