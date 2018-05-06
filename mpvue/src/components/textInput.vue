<template>
  <div class="form-cell">
    <db-label :value='label'></db-label>
    <input :type="type" class="form-control" :placeholder="placeholder" :focus='focus' :disabled='disabled' :value='value' :name='name' />
  </div>
</template>

<script>
  import label from '@/components/label'
  export default {
    props: {
      placeholder: String,
      disabled: Boolean | String,
      focus: Boolean | String,
      type: String,
      label: String,
      value: String,
      name: String
    },
    components: {
      'db-label': label
    },
    onLoad () {
      console.log('加载')
    }/* ,
    created () {
      console.log('created')
    },
    mounted () {
      console.log('mounted')
    } */
  }
</script>

<style>
  @import '../assets/styles/bootstrap.wxss';
</style>
