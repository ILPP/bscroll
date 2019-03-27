<template>
  <div>
    <p>第一次成功的better-scroll</p>
    <scroll class="wrapper"
          :data="data"
          :pulldown="pulldown"
          @pulldown="loadData">
      <ul class="content">
        <li v-for="item in data">{{item}}</li>
      </ul>
      <div class="loading-wrapper"></div>
    </scroll>
  </div>
</template>
<script>
  import BScroll from 'better-scroll'
  import scroll from '@/components/base/scroll'
  export default {
    data() {
      return {
        data: [],
        pulldown: true,
        list: [],
        num: 0,
      }
    },
    created() {
      this.loadData()
    },
    components: {
      scroll
    },
    methods: {
      loadData() {
        alert(this.num)
        for(var i = 0; i < 20;i++) {
          this.list.push(`我是第${this.num}数据`)
        }
        this.data = this.data.concat(this.list)
        this.num++
      }
    }
  }
</script>


<style type="text/css" scoped>
  p {
    height: 60px;
    margin: 0;
    padding: 0;
  }
  .content li {
    margin: 10px 0;
  }
  .wrapper {
    position: fixed;
    z-index: 1;
    top: 60px;
    bottom: 50px;
    left: 0;
    width: 100%;
    background: #ccc;
    overflow: hidden;
  }
</style>