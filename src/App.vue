<template>
<div>
<router-view></router-view>
<FooterGuide></FooterGuide> 
</div>
</template>

<script type="text/ecmascript-6">
// 引入组件
import FooterGuide from "./components/FooterGuide/FooterGuide"

export default {
    components:{
        FooterGuide //注册组件
    }
}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">


</style>
