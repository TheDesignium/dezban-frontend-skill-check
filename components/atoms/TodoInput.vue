<template>
  <div>
    <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="username" type="text" placeholder="Input Todo item" :task="task" v-model="inputValue" @input="updateTask">
    {{inputValue}}
    </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data() {
    return {
      inputValue: ""
    }
  },
  props: ["task"],
  methods: {
    updateTask() {
      this.task = this.inputValue
      this.$emit('input', this.inputValue)
    }
  }
})
</script>