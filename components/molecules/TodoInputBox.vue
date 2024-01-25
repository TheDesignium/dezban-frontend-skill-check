<template>
  <div>
    <TodoInput />
    <Button />
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
  }
})
</script>