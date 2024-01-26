<template>
  <div class="flex flex-row">
    <TodoInput @input="updateTask" :task="task" />
    <Button text="add" class="ml-4" :onClick="addTask" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import TodoInput from '../atoms/TodoInput.vue'
import Button from '../atoms/Button.vue'

export default Vue.extend({
  components: {
    TodoInput,
    Button
  },
  props: ["addTask", "task"],
  methods: {
    updateTask(task) {
      this.$emit("input", task)
    }
  }
})
</script>