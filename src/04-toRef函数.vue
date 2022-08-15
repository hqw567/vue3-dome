<template>
  <div class="container">
    {{ info.name }}
    {{ info.age }}
    <h1>{{ name }}</h1>
    <button @click="updateName">修改名称</button>
  </div>
</template>

<script>
import { reactive, toRef } from 'vue'
export default {
  name: 'App',
  setup() {
    const info = reactive({
      name: 'Herway',
      age: 18
    })
    const name = toRef(info, 'name')
    const updateName = () => {
      console.log('updateName')
      name.value = 'Hello Word'
    }
    return { info, updateName, name }
  }
}
</script>

<style lang="scss" scoped>
</style>