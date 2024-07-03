<template >

   <div>
    
    <v-spacer />
    <div class="flex justify-center items-center  bg-blue-500 text-3xl">
    <p class ="my-2 "> TODOリスト</p>
    </div>
    <div class="bg-hero h-screen">
    <form @submit.prevent="addTodo">
      <input 
        v-model="newTodo" 
        required
        placeholder=" input new todo" 
        class="w-5/6 ml-8 mt-5 border-b-2  border-4 border-green-500 rounded
        "
      />
      <TodoButton title="add" :click-action="addTodo"></TodoButton>
    </form>

    <div class="list-disc ml-10 mt-4 text-red-400">
      <li v-for="todo in todos" :key="todo.id">
        {{ todo.text }}
        <TodoButton title="delete" :click-action="removeTodo" :todo="todo" />
      </li>
    </div>
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

<style scoped>
.body-bg{
  background-image:url('');
    background-repeat:  no-repeat;
    width: 100%;
    height: 100%;
    object-fit: cover;
}
</style>