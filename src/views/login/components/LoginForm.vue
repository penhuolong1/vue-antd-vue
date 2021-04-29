<template>
  <div class="w-full">
    <h1 class="font-bold text-3xl enter-X mb-6">登陆</h1>
    <Form :form="form">
      <FormItem class="enter-X">
        <Input v-model="form.name" size="large" placeholder="账号" />
      </FormItem>
      <FormItem class="enter-X">
        <Input v-model="form.name" type="password" size="large" placeholder="账号" />
      </FormItem>
      <FormItem class="enter-X">
        <Row type="flex" align="middle">
          <Col :span="12">
            <Checkbox v-model="rememberMe" size="small">
              记住我
            </Checkbox>
          </Col>
          <Col :span="12" class="text-right">
            <Button type="text">忘记密码?</Button>
          </Col>
        </Row>
      </FormItem>
      <FormItem class="enter-X">
        <Button type="primary" class="w-full">登陆</Button>
      </FormItem>
      <Row class="enter-X" type="flex" :gutter="20" align="middle">
        <Col :span="8">
          <Button size="small" class="w-full">手机登陆</Button>
        </Col>
        <Col :span="8">
          <Button size="small" class="w-full">二维码登陆</Button>
        </Col>
        <Col :span="8">
          <Button size="small" class="w-full">注册</Button>
        </Col>
      </Row>
      <Divider class="my-5 enter-X" text="其他登录方式" />
      <div class="flex enter-X">
        <Svg-icon icon-class="github" class="icon" />
        <Svg-icon icon-class="wx" class="icon" />
        <Svg-icon icon-class="zfb" class="icon" />
        <Svg-icon icon-class="google" class="icon" />
        <Svg-icon icon-class="twitter" class="icon" />
      </div>
    </Form>
  </div>
</template>

<script>
import { Form, FormItem, Input, Row, Col, Checkbox, Button } from 'element-ui'
import Divider from '@/components/Divider/index'
export default {
  components: {
    Form,
    FormItem,
    Input,
    Col,
    Row,
    Checkbox,
    Button,
    Divider
  },
  props: {

  },
  data() {
    return {
      form: {},
      rememberMe: false
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
/deep/ .inner-text{
  font-size: 12px;
  color: rgba(0, 0, 0, 0.45);
}
.icon {
  color: #888;
  flex: 1;
  font-size: 25px;
  cursor: pointer;
  &:hover {
    color: #0960bd;
  }
}
</style>
