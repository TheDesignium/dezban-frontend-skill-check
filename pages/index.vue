<template>
  <div>
    <v-spacer />
    <div class="flex justify-center items-center">
      <p>TODOリスト</p>
    </div>

    <form @submit.prevent="addTodo"> 
      
      <input v-model="newTodo" required placeholder="input new todo " class="width: w-96;"/> 
      <TodoButton title="add" :click-action="addTodo"></TodoButton>  
    </form>
  
    <div class="list-disc ">
      <li v-for="todo in todos" :key="todo.id" >
        {{ todo.text }}
        <TodoButton title="delete" :click-action="removeTodo" :todo="todo" />
      </li>
    </div>
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
        { id: this.id++, text: 'hoge' },
        { id: this.id++, text: 'huga' },
      ],
    }
  },
  methods: {
    addTodo() {
      this.todos.push({ id: this.id++, text: this.newTodo })
      this.newTodo = ''
    },
    removeTodo(todo) {
      this.todos = this.todos.filter((t) => t !== todo)
    },
  },
}
</script>
