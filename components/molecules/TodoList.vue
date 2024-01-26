<template>
  <div>
    <div v-for="value in tasks" :key="value.id" class="flex flex-row items-center my-2">
      <TodoItem :taskValue="value" />
      <Button text="delete" class="mx-3"/>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import TodoItem from '../atoms/TodoItem.vue'
import Button from '../atoms/Button.vue'

export default Vue.extend({
  components: {
    TodoItem,
    Button
  },
  props: ["tasks"]
})
</script>