<template>
  <div class="container">
    根组件
  </div>
</template>

<script>
import { onBeforeMount , onMounted} from 'vue'
export default {
  name: 'App',
  setup () {
   onBeforeMount(() => {
   console.log('Dom渲染前钩子',document.querySelector('.container')); 
  })
  onMounted(() => {
    console.log('Dom渲染后钩子',document.querySelector('.container'));
  })
  },
  
}
</script>

<style lang="scss" scoped>

</style>