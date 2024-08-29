<template>
  <div>
    <button class="text-700 border-2 border-500" @click="clickAction(todo)">
      {{ title }}
    </button>
  </div>
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
