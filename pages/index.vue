<template>
  <div>
    <v-spacer />
    <div class="flex justify-center items-center text-3xl">
      <p> TODOリスト </p>
    </div>

    <form class="flex items-center" @submit.prevent="addTodo">
      <input
        v-model="newTodo"
        placeholder="input new todo"
        class="w-5/6 m-3 border-b-2 border-2"
      />
      <TodoButton title="add" :click-action="addTodo"></TodoButton>
    </form>

    <ul class="list-disc m-3">
      <li v-for="todo in todos" :key="todo.id" class="flex items-center">
        <span>・ {{ todo.text }}</span>
        <TodoButton title="delete" :click-action="removeTodo" :todo="todo" />
      </li>
    </ul>
  </div>
</template>

<script>
import TodoButton from '~/components/TodoButton.vue'

export default {
  components: {
    TodoButton,
  },

  data() {
    return {
      id: 0,
      newTodo: '',
      todos: [
        
      ],
    }
  },
  methods: {
    addTodo() {
      if (this.newTodo.trim() !== '') {
        this.todos.push({ id: this.id++, text: this.newTodo })
        this.newTodo = ''
      }
    },
    removeTodo(todo) {
      this.todos = this.todos.filter((t) => t !== todo)
    },
  },
}
</script>

<style scoped>
.bg-white {
  background-color: white;
}
</style>
