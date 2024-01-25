<template>
  <div>
    <TodoInputBox />
    <TodoList />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import TodoInputBox from '../molecules/TodoInputBox.vue'
import TodoList from '../molecules/TodoList.vue'

export default Vue.extend({
  components: {
    TodoInputBox,
    TodoList
  }

})
</script>