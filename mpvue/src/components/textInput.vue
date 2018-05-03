<template>
  <div class="form-cell">
    <db-label :value='label'></db-label>
    <input :type="type" class="form-control" :placeholder="placeholder" />
  </div>
</template>

<script>
  import label from '@/components/label'
  export default {
    props: {
      placeholder: String,
      autoHeight: Boolean,
      state: String,
      type: String,
      label: String,
      value: String
    },
    components: {
      'db-label': label
    }
  }
</script>

<style>
  @import '../assets/styles/bootstrap.wxss';
</style>
