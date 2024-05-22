<template>
  <div>
    <TodoButton />
    <div>

    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import TodoButton from '../components/TodoButton.vue'

export default Vue.extend({
  name: 'IndexPage',
  components: {
    TodoButton,
  },
})
</script>
