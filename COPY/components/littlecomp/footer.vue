<template>
  <div class="footer">
    <ul class="clearfix">
      <li>
        <a v-on:click="setHash('/page/1')">
          <div class="icon_box" ><img src="../../assets/img/icon-1.png" :class="page.pageOne ? 'cur' : ''"/></div>
        </a>
        <p>图书</p>
      </li>
      <li>
        <a v-on:click="setHash('/page/2')">
          <div class="icon_box" ><img src="../../assets/img/icon-2.png" :class="page.pageTwo ? 'cur' : ''"/></div>
        </a>
        <p>推荐</p>
      </li>
      <li>
        <a v-on:click="setHash('/page/3')">
          <div class="icon_box" ><img src="../../assets/img/icon-3.png" :class="page.pageThree ? 'cur' : ''"/></div>
        </a>
        <p>我的</p>
      </li>
    </ul>
  </div>
</template>
<script>
  export default{
     name:'foot',
    props: ['parentPage'],
    data () {
       return {
        page:this.parentPage
       }
    },
    methods:{
      setHash:function(x){
        this.$router.replace({path:x});
//        switch (x){
//          case '/page/1':
//            this.page.pageOne = true;
//            this.page.pageTwo = this.page.pageThree = false;
//            break;
//          case '/page/2':
//            this.page.pageTwo = true;
//            this.page.pageOne = this.page.pageThree = false;
//            break;
//          case '/page/3':
//            this.page.pageThree = true;
//            this.page.pageOne = this.page.pageTwo = false;
//            break;
//        }
      }
    }
  }
</script>
