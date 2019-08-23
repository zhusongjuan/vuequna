<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
            <!-- slides -->
            <swiper-slide v-for="item in swiperList" :key="item.id">
                <img class="swiper-img" alt="" :src="item.imgUrl">
            </swiper-slide>
          
            <!-- Optional controls -->
            <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
    </div>
</template>
<script>
export default {

    data(){
        return {
            swiperOption:{
                pagination: '.swiper-pagination',
                loop: true
            },
            swiperList:[
                {
                    id:1,
                    imgUrl:'//mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/3f5ff03fa0c024b930f515e63ae2c702.jpg_945x288_7dff4510.jpg'
                },{
                    id:2,
                    imgUrl:'//mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/b72df47942fb28fcd7bf481f01e785f5.jpg'
                }
            ]
        }
    }
}
</script>
<style lang="stylus" scoped>
// 修饰全局样式
.wrapper >>> .swiper-pagination-bullet-active
    background: #fff
.wrapper
    width 100%
    height 0
    overflow hidden
    padding-bottom:31.25%
    .swiper-img 
        width 100%
</style>