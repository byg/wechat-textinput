<template>
  <div class="container" @click="clickHandle('test click', $event)">
    <form class="form-container">
        <text-input name='username' type='text' placeholder='I am placeholder' label='用户名' />
        <text-input name='username' type='text' placeholder='自动聚焦' focus='false' label='文本' />
        <text-input name='text' type='text' placeholder='输入文字' label='文本' />
        <text-input name='number' type='number' placeholder='只能输入数字' label='数字' />
        <text-input name='email' type='email' placeholder='输入邮箱' label='邮箱' />
        <text-input name='idCard' type='idCard' placeholder='输入身份证' label='身份证' />
        <text-input name='digit' type='digit' placeholder='数字带小数点' label='小数' />
        <text-input name='username' type='text' value='输入框已禁用' disabled='true' label='文本' />
        <text-input name='username' type='text' readOnly='true' plainText='true' placeholder='显示为普通为本' label='文本' value='显示为普通为本'/>
        <text-input name='username' type='text' maxLength='6' placeholder='最多只能输入6位' label='文本' />
    </form>
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
    'text-input': textInput
  },

  methods: {
    bindViewTap () {
      const url = '../logs/main'
      wx.navigateTo({ url })
    },
    getUserInfo () {
      // 调用登录接口
      wx.login({
        success: () => {
          wx.getUserInfo({
            success: (res) => {
              this.userInfo = res.userInfo
            }
          })
        }
      })
    },
    clickHandle (msg, ev) {
      console.log('clickHandle:', msg, ev)
    }
  },

  created () {
    // 调用应用实例的方法获取全局数据
    this.getUserInfo()
  }
}
</script>

<style scoped>
.userinfo {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.userinfo-avatar {
  width: 128rpx;
  height: 128rpx;
  margin: 20rpx;
  border-radius: 50%;
}

.userinfo-nickname {
  color: #aaa;
}

.usermotto {
  margin-top: 150px;
}

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
