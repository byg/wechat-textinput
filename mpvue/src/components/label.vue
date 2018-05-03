<template>
    <label class='form-label'>{{value ? value : ''}}</label>
</template>

<script>
  export default {
    props: {
      value: String
    }
  }
</script>

<style>
  @import '../assets/styles/bootstrap.wxss';
</style>
