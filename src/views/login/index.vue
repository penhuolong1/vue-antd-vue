<template>
  <div :class="sysName+'-login'" class="w-full h-full flex">
    <div class="flex-1 h-full">
      <div :class="sysName+'logo'" class="flex">
        <img src="logoImg" alt="">
        <div class="title" />
      </div>
    </div>
    <div class="flex-1 h-full">右边</div>
  </div>
</template>

<script>
import { SYS_NAME } from '@/utils/variables.js'
export default {
  components: {

  },
  props: {

  },
  data() {
    return {
      sysName: SYS_NAME,
      logoImg: require('@/assets/logo.png')
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
@prefix-cls: ~'@{namespace}-login';
.@{prefix-cls} {
  overflow: hidden;
  &>div:first-child {
    background-image: url('../../assets/svg/login-bg.svg');
    background-repeat: no-repeat;
    background-size: auto 100%;
    background-position: 100%;
  }
}
</style>
