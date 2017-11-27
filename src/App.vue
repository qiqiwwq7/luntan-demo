<template>
  <div id="app">
    <header class='luntan-header'>
       <div class=''></div>
    </header>
    <div class="luntan">
        <router-view/>
    </div>
  </div>
</template>
<script>
import { Icon } from 'vux'
export default {
  name: 'app',
  components: {
    Icon
  }
}
</script>
<style lang='less'>
@import url('./assets/css/pink.less');

/* 公共 */
.luntan-header {
  background: #1A2946;
}
.luntan {
  width: 100%;
  height: 100%;
}
/*横屏  */
@media all and (orientation: landscape) {
  .luntan-header {
    width: 60px;
    height:100%;
    float: left;
  }
}
/*竖屏  */
@media all and (orientation: portrait) {
  .luntan-header {
    width: 100%;
    height:60px;
    position: absolute;
    left: 0;
    bottom:0;
  }
}
</style>
