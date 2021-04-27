<template>
  <div :class="sysName+'-logo'" class="flex items-center font-semibold">
    <img :src="logoImg" alt="" :class="imgWidth">
    <div class="title text-white ml-2.5 font-bold" :class="fontSize">{{ sysName+' Admin' }}</div>
  </div>
</template>

<script>
import { SYS_NAME } from '@/utils/variables.js'
export default {
  components: {

  },
  props: {
    imgWidth: { // 图片宽度
      type: String,
      default: ''
    },
    fontSize: { // 标题字体大小
      type: String,
      default: ''
    }
  },
  data() {
    return {
      sysName: SYS_NAME,
      logoImg: require('@/assets/images/logo.png')
    }
  },
  created() {

  },
  mounted() {

  },
  methods: {

  }
}
</script>

<style scoped lang="less">

</style>
