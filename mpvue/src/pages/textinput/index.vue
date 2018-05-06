<template>
  <div class="container">
      <text-input name='default' type='text'  label='文本' />
      <text-input name='username' type='text' placeholder='I am placeholder' label='用户名' />
      <text-input name='text' type='text' placeholder='输入文字' label='文本' />
      <text-input name='number' type='number' placeholder='只能输入数字' label='数字' />
      <text-input name='email' type='email' placeholder='输入邮箱' label='邮箱' />
      <text-input name='idCard' type='idCard' placeholder='输入身份证' label='身份证' />
      <text-input name='digit' type='digit' placeholder='数字带小数点' label='小数' />
      <text-input name='username1' type='text' value='输入框已禁用' disabled='true' label='文本' />
      <text-input name='username2' type='text' maxLength='6' placeholder='最多只能输入6位' label='文本' />
  </div>
</template>

<script>
import textInput from '@/components/textInput'
export default {
  data () {
    return {
      motto: 'Hello World',
      userInfo: {}
    }
  },

  components: {
    'text-input': textInput,
    'text-input1': textInput,
    'text-input2': textInput,
    'text-input3': textInput,
    'text-input4': textInput,
    'text-input5': textInput,
    'text-input6': textInput,
    'text-input7': textInput,
    'text-input8': textInput,
    'text-input9': textInput,
    'text-input10': textInput,
    'text-input11': textInput,
    'text-input12': textInput,
    'text-input13': textInput,
    'text-input14': textInput,
    'text-input15': textInput,
    'text-input16': textInput,
    'text-input17': textInput,
    'text-input18': textInput,
    'text-input19': textInput
  }
}
</script>

<style scoped>
.form-control {
  display: block;
  padding: 0 12px;
  margin-bottom: 5px;
  border: 1px solid #ccc;
}

.counter {
  display: inline-block;
  margin: 10px auto;
  padding: 5px 10px;
  color: blue;
  border: 1px solid blue;
}
</style>
