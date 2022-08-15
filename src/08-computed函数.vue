<template>
  <div class="container">
    <div>今年：{{ age }}岁</div>
    <div>后年：{{ newAge }}岁</div>
    <input type="text" v-model="newAge" />
  </div>
</template>

<script>
import { ref, computed } from 'vue'
export default {
  name: 'App',
  setup() {
    const age = ref(18)
    // const newAge = computed(() => age.value + 2)
    const newAge = computed({
      get() {
        return age.value + 2
      },
      set(v) {
        age.value = v - 2
      }
    })
    return { age, newAge }
  }
}
</script>

<style lang="scss" scoped>
</style>