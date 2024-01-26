<template>
  <div>
    <TodoInputBox :addTask="addTask" :task="task" @input="updateTask" class="m-14" />
    <TodoList class="mx-16" :tasks="tasks" />
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
  },
  data() {
    return {
      task: "",
      tasks: []
    }
  },
  methods: {
    addTask(task: string) {
      this.tasks.push(this.task)
      this.task = ""
      console.log(this.tasks)
    },
    updateTask(task) {
      this.task = task
    },
  }
})
</script>