<template>
  <li class="text-xl">{{taskValue}}</li>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: ["taskValue"]
})
</script>