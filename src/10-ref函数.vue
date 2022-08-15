<template>
  <div>
    <!-- vue2 ref写法 -->
    <!-- <div ref="box">box</div>
    <div ref="box2">box2</div>
    <div ref="box3">box3</div>
    <ul>
      <li v-for="i in 4" :key="i" ref="li">{{ i }}</li>
    </ul> -->
    <div ref="box">box</div>
    <ul>
      <li v-for="i in 4" :key="i" ref="li">{{ i }}</li>
    </ul>
  </div>
</template>

<script>
import { onMounted, ref } from 'vue'
export default {
  name: 'App',
  setup() {
    const box = ref(null)
    const li = ref(null)
    onMounted(() => {
      console.log(box.value)
      console.log([...li.value])
    })
    return { box, li }
  }
}
</script>

<style lang="scss" scoped>
</style>