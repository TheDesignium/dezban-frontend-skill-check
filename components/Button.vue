<template>
  <div>
    <button @click="onClick(index)" class="h-10 w-20 border rounded">{{text}}</button>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: {
    text: {
      type: String,
      default: ""
    },
    onClick: {
      type: Function,
      default: () => {}
    },
    index: {
      type: Number,
      default: 0
    }
  }
})
</script>