<template>
  <div class="w-full">
    <h1 class="font-bold text-3xl enter-X mb-6">登陆</h1>
    <Form :form="form">
      <FormItem>
        <Input v-model="form.name" size="large" placeholder="账号" />
      </FormItem>
      <FormItem>
        <InputPassword v-model="form.name" size="large" placeholder="账号" />
      </FormItem>
      <ARow class="enter-X" type="flex" align="center">
        <ACol :span="12">
          <Checkbox v-model="rememberMe" size="small">
            记住我
          </Checkbox>
        </ACol>
        <ACol :span="12" class="text-right">
          <Button type="link">忘记密码?</Button>
        </ACol>
      </ARow>
      <FormItem class="enter-x">
        <Button type="primary">登陆</Button>
      </FormItem>
    </Form>
  </div>
</template>

<script>
import { Form, Input, Row, Col, Checkbox, Button } from 'ant-design-vue'
export default {
  components: {
    Form,
    FormItem: Form.Item,
    Input,
    InputPassword: Input.Password,
    [Col.name]: Col,
    [Row.name]: Row,
    Checkbox,
    Button
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

<style scoped lang="scss">

</style>
