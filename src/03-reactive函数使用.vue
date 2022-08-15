<template>
  <div class="container">
    {{info.name}}
    {{info.age}}
    <button @click="updateName">修改名称</button>
  </div>
</template>

<script>
import { reactive } from "vue"
export default {
  name: 'App',
  setup () {
  const info = reactive({
    name: 'Herway',
    age: 18
  })
  const updateName = () => {
    info.name = 'Hello Word'
  }
    return { info ,updateName}
  },

}
</script>

<style lang="scss" scoped>

</style>