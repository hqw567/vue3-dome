<template>
  <div>
    <h1>父组件</h1>
    <hr />
    <Son :msg="msg" />
  </div>
</template>

<script>
import { ref } from 'vue'
import Son from './11-son.vue'
export default {
  components: {
    Son
  },
  setup() {
    const msg = ref('Fu')
    return { msg }
  }
}
</script>

<style lang="scss" scoped>
</style>