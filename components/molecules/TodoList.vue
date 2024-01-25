<template>
  <div>
    <TodoItem />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import TodoItem from '../atoms/TodoItem.vue'
export default Vue.extend({
  components: {
    TodoItem
  }
})
</script>