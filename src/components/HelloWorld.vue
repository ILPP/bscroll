<template>
  <scroll class="wrapper"
          :data="data"
          :pulldown="pulldown"
          @pulldown="loadData">
    <ul class="content">
      <li v-for="item in data">{{item}}</li>
    </ul>
    <div class="loading-wrapper"></div>
  </scroll>
</template>
<script>
  import BScroll from 'better-scroll'
  import scroll from '@/components/base/scroll'
  export default {
    data() {
      return {
        data: [],
        pulldown: true,
        list: [
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
          '我是第一条数据',
        ]
      }
    },
    created() {
      this.loadData()
    },
    conponents: {
      scroll
    },
    methods: {
      loadData() {
        this.data.concat(this.list)
      }
    }
  }
</script>


<style type="text/css" scoped>
  p {
    height: 30px;
    font-size: 24px;
    line-height: 30px;
    text-align: center;
    padding: 10px 0;
  }
  .wrap {
    max-height: 100vh;
  }
</style>