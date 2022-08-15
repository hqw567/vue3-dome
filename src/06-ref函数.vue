<template>
  <div class="container">
    <h1>{{ name }}</h1>
    <h1>{{ age }}</h1>
    <button @click="updateName">修改name</button>
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
  name: 'App',
  setup() {
    const name = ref('Herway')
    const age = ref(18)
    console.log(name)
    const updateName = () => {
      name.value = 'Update'
    }
    return { name, age, updateName }
  }
}
</script>

<style lang="scss" scoped>
</style>