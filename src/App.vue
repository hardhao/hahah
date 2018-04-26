<template>
  <div class="home">
    <router-view></router-view>
  </div>

</template>

<script>
import Post from './components/Post'

export default {
  name: 'app',
  components: {
    Post
  }
}
</script>
<style>
*{
  box-sizing: border-box;
}
body {
  margin: 0;
}
</style>
