<template>
  <img 
  class="avatar-container"
  :src="url" 
  :style="{
      width:size + 'px',
      height:size + 'px',
      borderRadius:percent + '%',
  }">
</template>

<script>
export default {
    name: "avatar",
    props:{
        url: {
        type:String,
        required: true, //属性必传
        },
        size:{
        type: Number,
        default: 150,
        },
        percent:{
        type: Number,
        default:50,
        }
      
    }
}
</script>

<style scoped>
    /* scoped样式作用域 */
    /* 现在测试mac端改变。windows同步过去 */
    /* windows端 直接 git pull 成功 */
    /* 第二次测试windows端改变，mac同步 */
    .avatar-container{      
        display: block;
        object-fit: cover;
    }
</style>