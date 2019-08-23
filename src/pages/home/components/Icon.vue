<template>
    <div class="icons">
        <swiper>
            <swiper-slide v-for="(page,index) of pages" :key="index">
                <div class="icon" v-for="item of page" :key="item.id">
                    <div class="icon-img">
                        <img class="icon-img-content" :src="item.imgUrl"/>
                    <p class="icon-desc">热门推荐</p>
                    </div>
                </div>
            </swiper-slide>
        </swiper>
    </div>
</template>
<script>
export default {
    data(){
        return {
            iconList:[
                {
                    id:1,
                    imgUrl:"//s.qunarzz.com/homenode/images/touchheader/hotel.png"
                },
                  {
                    id:2,
                    imgUrl:"//s.qunarzz.com/homenode/images/touchheader/hotel.png"
                },
                 {
                    id:3,
                    imgUrl:"//s.qunarzz.com/homenode/images/touchheader/hotel.png"
                },
                 {
                    id:4,
                    imgUrl:"//s.qunarzz.com/homenode/images/touchheader/hotel.png"
                },
                 {
                    id:5,
                    imgUrl:"//s.qunarzz.com/homenode/images/touchheader/hotel.png"
                },
                 {
                    id:6,
                    imgUrl:"//s.qunarzz.com/homenode/images/touchheader/hotel.png"
                },
                 {
                    id:7,
                    imgUrl:"//s.qunarzz.com/homenode/images/touchheader/hotel.png"
                },
                 {
                    id:8,
                    imgUrl:"//s.qunarzz.com/homenode/images/touchheader/hotel.png"
                },
                 {
                    id:9,
                    imgUrl:"//s.qunarzz.com/homenode/images/touchheader/hotel.png"
                },
                 {
                    id:10,
                    imgUrl:"//s.qunarzz.com/homenode/images/touchheader/hotel.png"
                },

            ]
        }
    },
    computed:{
        pages (){
            const pages = []
            this.iconList.forEach((item,index)=>{
                 const page = Math.floor(index / 8)
                 if(!pages[page]){
                     pages[page] = []
                 }
                 pages[page].push(item)
            })
            return pages
        }
    }
}
</script>
<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.styl'
.icons >>> .swiper
    overflow:hidden
    height:0
    padding-bottom:50%
.icon
    float:left
    width:25%
    height 0
    padding-bottom:25%
    position relative
    .icon-img
        position absolute
        top 0
        left 0
        right 0
        bottom .44rem
        box-sizing border-box
        padding .1rem
        .icon-img-content
            height 100%
            display block
            margin 0 auto 
        .icon-desc
            position absolute
            left 0
            right 0
            bottom -.44rem
            line-height .44rem
            height .44rem
            color:$darkTextColor
            text-align center
</style>