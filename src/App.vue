<template>
  <div id="app" :class="rootClass">
    <header class='luntan-header'>
        <div class='shouye'>首页</div>
        <div class='luntan'>论坛</div>
        <div class='luntan'>论坛</div>
        <div class='luntan'>论坛</div>
    </header>
    <div class="luntan">
        <!-- <group>
          <selector title="title" @on-change="changeTheme" :options="options" v-model="theme"></selector>
        </group>
        <group>
          <calendar :readonly="readonly" v-model="demo1" :title="'Basic Usage'" disable-past placeholder="placeholder" @on-show="log('show')" @on-hide="log('hide')"></calendar>
        </group>
        <button-tab>
          <button-tab-item>Today</button-tab-item>
          <button-tab-item selected>This Week</button-tab-item>
          <button-tab-item>This Month</button-tab-item>
        </button-tab> -->
        <router-view/>
    </div>
  </div>
</template>
<script>
import { Icon, Selector, Group, Calendar, ButtonTab, ButtonTabItem } from 'vux'
export default {
  name: 'app',
  data () {
    return {
      theme: null,
      options: [
        {
          key: 0,
          value: 'default'
        },
        {
          key: 1,
          value: 'primary'
        },
        {
          key: 2,
          value: 'red'
        }
      ],
      rootClass: 'app-default',
      // Calendar 参数设置
      readonly: false,
      demo1: ''
    }
  },
  components: {
    Icon,
    Selector,
    Group,
    Calendar,
    ButtonTab,
    ButtonTabItem
  },
  methods: {
    changeTheme (data) {
      // console.log('*****data', data)
      this.options.forEach(item => {
        if (item.key === data) {
          this.rootClass = `app-${item.value}`
        }
      })
    },
    log (str) {
      console.log(str)
    },
    onChange (val) {
      console.log('on change', val)
    }
  }
}
</script>
<style lang='less'>
  // .luntan-header {
  //   width: 100%;
  //   height:60px;
  //   position: fixed;
  //   left: 0;
  //   bottom:0;
  //   display: flex;
  //   div {
  //     width: 100%;
  //     height: 100%;
  //     flex-direction: column;
  //   }
  // }
/*横屏  */
@media all and (orientation: landscape) {
  // .luntan-header {
  //   width: 60px;
  //   height:100%;
  //   float: left;
  // }
  .luntan-header {
    width: 60PX;
    height:100%;
    position: fixed;
    left: 0;
    bottom:0;
    display: flex;
    flex-direction:column-reverse;
    div {
      width: 100%;
      height: 100%;
      // flex-direction:row-reverse;
      display: flex;
  align-items: center;
    }
  }
}
/*竖屏  */
@media all and (orientation: portrait) {
  // .luntan-header {
  //   width: 100%;
  //   height:60px;
  //   position: fixed;
  //   left: 0;
  //   bottom:0;
  // }
    .luntan-header {
    width: 100%;
    height:60px;
    position: fixed;
    left: 0;
    bottom:0;
    display: flex;
    align-items: center;
    div {
      width: 100%;
      height: 100%;
      flex-direction: column;
      display: flex;
      align-items: center;
      line-height: 60px;
    }
  }
}
</style>
