<template>
  <div>
    <ul class="type">
      <li>官方公告</li>
      <li>最新发帖</li>
      <li>最新回复</li>
    </ul>
  </div>
</template>
<script>
// import { Group, Cell, DatetimeRange } from 'vux'
export default {
  name: 'HelloWorld',
  data () {
    return {
       // kk
    }
  },
  components: {
    // kk
  },
  methods: {
  // kk
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
.type {
  width: 100%;
  height: 50px;
  background: #1A2946;
  li {
    padding: 0 10px;
    float: left;
    background: #1A2946;
    color: #fff;
    line-height: 50px;
    cursor: pointer;
  }
  li:hover {
    color: #CE7E03;
    border-bottom: 1px solid #CE7E03;
    background: #081529;
  }
}
/*横屏  */
@media all and (orientation: landscape) {

}
/*竖屏  */
@media all and (orientation: portrait) {

}
</style>
