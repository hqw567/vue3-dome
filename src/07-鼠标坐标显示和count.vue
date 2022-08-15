<template>
  <div class="container">
    <h1>鼠标X{{ x }}</h1>
    <h1>鼠标Y{{ y }}</h1>
    <hr />
    <h1 style="color: red">{{ num }}</h1>
    <button @click="add">加数字</button>
  </div>
</template>

<script>
import { onMounted, ref, toRefs, reactive, onUnmounted } from 'vue'
export default {
  name: 'App',
  setup() {
    const mouse = reactive({
      x: 0,
      y: 0
    })
    onMounted(() => {
      document.addEventListener('mousemove', (e) => {
        mouse.x = e.pageX
        mouse.y = e.pageY
      })
    })
    onUnmounted(() => {
      document.removeEventListener('mousemove', () => {})
    })
    const num = ref(0)
    const add = () => {
      num.value++
    }
    return { ...toRefs(mouse), num, add }
  }
}
</script>

<style lang="scss" scoped>
</style>