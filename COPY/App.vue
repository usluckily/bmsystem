<template>
    <!--<img src="./assets/logo.png">-->
    <router-view></router-view>
</template>

<script>
  import {NI} from '@/assets/js/nodeInit'
  import foot from '@/components/littlecomp/footer'
  import $ from 'jquery'

  export default {
    name: 'app',
    components:{
      my_foot:foot
    },
    methods:{
      Init:function(){
        NI().rootFontSize();
      }
    },
    created () {
      this.Init();
      //屏蔽ios下上下弹性
//      $(window).on('scroll.elasticity', function (e) {
//        e.preventDefault();
//      }).on('touchmove.elasticity', function (e) {
//        e.preventDefault();
//      });
    },
    mounted () {
      //do something...
    }
  }
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
<style src="./assets/css/base.css"></style>
<style src="./assets/css/swiper-3.3.1.min.css"></style>
