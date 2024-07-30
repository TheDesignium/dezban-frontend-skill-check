<template>
  <div>
    <div class="h-14 shadow flex justify-center items-center">
    <p class="text-2xl">
      TODOリスト
    </p>
  </div>
    <div class="body">
      <div class="flex m-10">
        <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="username" type="text" placeholder="Input Todo item" v-model="task">
        <Button text="add" :onClick="addTask" class="ml-5" />
      </div>
      <div class="flex mx-10 mb-3 items-center " v-for="(value, i) in tasks" :key="value.id">
        <li class="text-xl">{{value}}</li>
        <Button class="ml-4" text="delete" :onClick="deleteTask" :index="i"/>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Button from '../components/Button.vue'

export default Vue.extend({
  name: 'IndexPage',
  components: {
    Button
  },
  data(){
    return {
      task: "",
      tasks: ["hoge", "huga"]
    }
  },
  computed: {
  },
  methods: {
    addTask() {
      if(this.task.trim() !== ""){
        this.tasks.push(this.task)
      }
        this.task = ""
    },
    deleteTask(i: number) {
      this.tasks.splice(i, 1)
    }
  }
})
</script>
