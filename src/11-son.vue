<template>
  <div>
    <h1>子组件{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'Son',
  props: {
    msg: {
      type: String,
      default: 'Son'
    }
  },
  setup() {}
}
</script>

<style lang="scss" scoped>
</style>