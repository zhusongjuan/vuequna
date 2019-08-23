<template>
  <div id="app">
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icon></home-icon>
  </div>
</template>
<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcon from './components/Icon'
export default {
  components:{
    HomeHeader,
    HomeSwiper,
    HomeIcon
  }
}
</script>
<style>
</style>
