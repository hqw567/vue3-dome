<template>
  <div class="container">
    <h1 @click="say">{{msg}}</h1>
  </div>
</template>

<script>
export default {
  name: 'App',
  setup () {
    const say = () => {
      console.log('Hello Vue3');
    }
    const msg = 'Welcome to Vue3'
    return {
      msg,say
    }
  },
  beforeCreate() {
    console.log('beforeCreate',this);
  }
}
</script>

<style lang="scss" scoped>

</style>