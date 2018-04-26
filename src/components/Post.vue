<template>
  <div class="post">
    <div class="upper">
      <PostBody :title="title"/>
    </div>
    <div class="bottom">
      <CommentBox />
    </div>
  </div>
</template>

<script>
  import PostBody from './PostBody'
  import CommentBox from './CommentBox'

  export default {
    name: 'Post',
    data:() => ({
      title:'Git Tricks'
    }),
    components: {
      PostBody,
      CommentBox
    }
  }


</script>

<style scoped>
  .post {
    display: flex;
    flex-direction: column;
    height: 100vh;
  }
  .upper {
    display: flex;
    background-color: #53a6ae;
  }
  .bottom {
    height: 60vh;
    display: flex;
    flex-grow: 1;
  }
</style>
