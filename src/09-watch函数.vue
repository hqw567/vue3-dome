<template>
  <div class="container">
    <div>{{ count }}</div>
    <button @click="add">+1</button>
    <hr />
    <div>{{ obj.name }}</div>
    <button @click="updateName">修改</button>
  </div>
</template>

<script>
import { ref, watch, reactive } from 'vue'
export default {
  name: 'App',
  setup() {
    const count = ref(0)
    const add = () => count.value++

    const obj = reactive({
      name: 'he'
    })
    const updateName = () => {
      obj.name = 'update'
    }
    // watch(obj, (newV, oldV) => {
    //   console.log(newV, oldV)
    // })
    // watch(count, (newV, oldV) => {
    //   console.log(newV, oldV)
    // })

    // watch([count, obj], (newV, oldV) => {
    //   console.log('数据变化了')
    // })

    watch(
      () => obj.name,
      (newV, oldV) => {
        console.log('name数据变化了')
      },
      { deep: true, immediate: true }
    )
    return { count, add, updateName, obj }
  }
}
</script>

<style lang="scss" scoped>
</style>