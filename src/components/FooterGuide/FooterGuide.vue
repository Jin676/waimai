<template>
<div class="footer-guide">
 <span class="guide-item " :class="{on: $route.path === '/msite'}" @click="goto('/msite')"> 
     <span>
         <i class="iconfont iconicon4 "></i>
     </span>
     <span>首页</span>
 </span>
 <span class="guide-item" :class="{on: $route.path === '/search'}" @click="goto('/search')">
     <span>
         <i class="iconfont iconsousuo"></i>
     </span>
     <span>搜索</span>
 </span>
 <span class="guide-item" :class="{on: $route.path === '/order'}" @click="goto('/order')">
     <span>
         <i class="iconfont icondingdan"></i>
     </span>
     <span>订单</span>
 </span>
 <span class="guide-item" :class="{on: $route.path === '/profile'}" @click="goto('/profile')">
     <span>
         <i class="iconfont iconwode"></i>
     </span>
     <span>我的</span>
 </span>
</div>
</template>

<script type="text/ecmascript-6">
export default {
    name:"FooterGuide",
    methods:{
        goto(path){
            this.$router.replace(path)
        }
    }

}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
   @import "../../common/stylus/mixins.styl"
   .footer-guide
    top-border-1px(#cccccc)//这个放前后对布局有影响，建议放最前面
    display flex 
    position fixed
    left 0
    bottom 0
    height 50px
    width 100%
    .guide-item
        display flex
        flex-direction column
        text-align center  
        width 25%   
      .on //&父级引用失效，所以没加
      color $green    
    span  
        margin-top 3px
        font-size 12px   
    i 
     font-size 22px
    
</style>
