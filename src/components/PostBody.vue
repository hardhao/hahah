<template>
  <div class="post-body">
    {{ title }}
  </div>
</template>
<script>
  export default {
    name: 'PostBody',
    props: ['title'],
  }
</script>



<style scoped>
  .post-body {
    width:400px;
    height: 80%;
    margin: 0 auto;
    margin-top: 20px;
    text-align: center;
    line-height:230px;
    background-color: #fff;
    margin-bottom: 20px;
  }
</style>
