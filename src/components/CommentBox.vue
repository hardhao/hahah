<template>
  <div class="wrap">
      <input v-model="msg" type="text" id="hhh" placeholder="请讲">
      <button @click="clickdeComments" id="xxx">提交</button>
      <div v-bind:key="comment.id" v-for="comment in reversedComments">
        {{ comment.body }}
        {{ reversedComments.body }}
      </div>
  </div>
</template>

<script>
  export default {
    name: 'CommentBox',
    data:() => ({
        msg:'',
        comments:[
            {
                id:'1',
                body:'cool'
            },
            {
                id:'2',
                body:'very cool'
            }
        ]
    }),
    computed:{
        reversedComments: function(){
            return this.comments.slice().reverse()
        }
    },
    methods:{
        clickdeComments:function(){
            console.log('clicked',this.msg)
            this.comments = [
            ...this.comments,
            {
                id:(this.comments.length + 1).toString(),
                body:this.msg
            }]
            this.msg = ''
         }
    }
  }
</script>

<style scoped>
  .wrap{
    background-color: #fff;
    width: 400px;
    margin: 20px auto;
    box-shadow: 0 2px 2px rgba(0, 0, 0, 0.5);
    border: 1px solid lightblue;
  }
  #hhh{
      width: 82%;
      text-indent:5px;
      margin-left:15px;
      flex-grow: 1;
  }
  #xxx{
      float: right;
  }
</style>