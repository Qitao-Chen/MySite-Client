<template>
<div class="blog-detail-container">
 <h1 class="devcom">BlogDetail => child components of "Detail"</h1>
 <h1>{{blog.title}}</h1>
 <div class="aside">
     <span>Date:{{blog.createDate}}</span>
     <span>Views:{{blog.scanNumber}}</span>
     <a href="#data-form-container"><span>Comments:{{blog.commentNumber}}</span></a>
     <RouterLink
     :to="{
         name:'CategoryBlog',
         params:{categoryId:blog.category.id}
     }"
     ><span>{{blog.category.name}}</span> </RouterLink>
 </div>
 <div v-html="blog.htmlContent">
     
 </div>

</div>
 
</template>

<script>
import "@/styles/markdown.css";
export default {
props:{
    blog:{
        type:Object,
        required:true,
    }
}
}
</script>

<style lang="less" scoped>
@import url(~@/styles/var.less);
.devcom{
    display: none;
}
.blog-detail-container{
   .aside{
    font-size: 12px;
    color:@grey;
    span{
      margin-right: 15px;
    }
}
}
</style>

