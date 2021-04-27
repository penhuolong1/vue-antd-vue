<template>
  <div :class="sysName+'-login'" class="w-full h-full flex red">
    <div class="flex flex-col flex-1 h-full p-14">
      <AppLogo class="pl-36 -enter-X" font-size="text-xl" img-width="w-12" />
      <div class="my-auto pl-36">
        <img :src="loginImg" class="w-2/3 -enter-X" alt="">
        <div class="text-white text-3xl mt-14 -enter-X">开箱即用的中后台管理系统</div>
        <div class="text-white text-sm mt-2 -enter-X">输入您的个人详细信息开始使用！</div>
      </div>
    </div>
    <div class="flex-1 h-full p-20 flex justify-center items-center">
      <div :class="sysName+'-form'" class="w-3/4 enter-X">
        <LoginForm />
      </div>
    </div>
  </div>
</template>

<script>
import { SYS_NAME } from '@/utils/variables.js'
import AppLogo from '@/components/AppLogo'
import LoginForm from './components/LoginForm'
export default {
  components: {
    AppLogo,
    LoginForm
  },
  props: {

  },
  data() {
    return {
      sysName: SYS_NAME,
      loginImg: require('@/assets/svg/login-box-bg.svg'),
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
@app-logo: ~'@{namespace}-logo';
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
