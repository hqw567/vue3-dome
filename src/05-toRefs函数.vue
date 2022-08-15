<template>
  <div class="container">
    <h1>{{ name }}</h1>
    <h1>{{ age }}</h1>
    <button @click="updateName">修改name</button>
  </div>
</template>

<script>
import { reactive, toRefs } from 'vue'
export default {
  name: 'App',
  setup() {
    const info = reactive({
      name: 'Herway',
      age: 18
    })
    console.log(info)
    const info2 = toRefs(info)
    const updateName = () => {
      info.name = 'Update'
    }
    return { ...toRefs(info), updateName }
  }
}
</script>

<style lang="scss" scoped>
</style>