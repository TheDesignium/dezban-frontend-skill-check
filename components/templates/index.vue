<template>
  <div>
    <Header />
    <Body />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Header from '../organisms/Header.vue'
import Body from '../organisms/Body.vue'

export default Vue.extend({
  components: {
    Header,
    Body
  }

})
</script>