<template>
    <div class="header">
        <div class="header-left">
            <span class="iconfont back-icon">&#xe624;</span>
        </div>
        <div class="header-input">
            <span class="iconfont">&#xe632;</span>
            输入城市/景点/游玩主题
        </div>
        <div class="header-right">
            城市
            <span class="iconfont arrow-icon">&#xe64a;</span>
        </div>
    </div>
</template>
<script>
export default {
    
}
</script>
<style lang="stylus" scoped>
// 二倍图 1rem=html font-size = 50px
@import '~@/assets/styles/varibles.styl';
.header
    display :flex
    line-height:.86rem
    background $bgColor
    color:#fff
    .header-left 
        width:.64rem
        float:left
        text-align:center
        .back-icon
            text-align center
            font-size .4rem
    .header-input
        flex :1
        background #fff
        border-radius:.1rem
        height .64rem
        line-height .64rem
        margin-top .12rem
        color #ccc
        margin-left .12rem
        padding-left .2rem
    .header-right
        width:1.24rem
        float:right
        text-align:center
        .arrow-icon
            // margin-left -.4rem
            font-size .24rem

</style>