<template>
  <view class="navigate-container"
        :style="{background:bgcolor,}"
        v-if='!hide'>
    <view :style="{height:statusBarHeight+'px'}"></view>
    <view v-if="!hideIconBar&&init"
          class="navigate-bar"
          :style="{color: fontColor,height:(navigationBarHeight-statusBarHeight) + 'px'}"
          :class="{'isIOS': isIOS}">
      <view class="navigate-icon"
            :style="{height:(navigationBarHeight-statusBarHeight) + 'px'}"
            hover-class="navigator-hover"
            @click="isShowHome?toHome():backPage()">
        <i class="iconfont icon-while-back icon-back4"
           v-if="!isShowHome"></i>
        <i class="iconfont icon-while-home icon-home"
           v-if="isShowHome"></i>
        <!-- :class="{'black-icon':isblack}" -->
      </view>
      <!--区分android、ios的字体 -->
      <view class="navigate-title container_flex row center"
            :class="{'androidTitle': !isIOS}">{{title}}</view>
    </view>
  </view>
</template>

<script >

export default {
  /**
    @isShowHome 是否展示 home 按钮
    @navigationBarHeight 导航栏高度
    @bgcolor 背景颜色
    @title 页面标题
    @callbackFun home 按钮点击事件
    @fontColor 字体颜色
    @hideIconBar 隐藏自定义导航栏
  */
  props: ['isShowHome', 'navigationBarHeight', 'bgcolor', 'title', 'callbackFun', 'fontColor', 'hideIconBar'],
  data () {
    return {
      isIOS: true, // ios风格
      statusBarHeight: 0, // 状态栏高度
      init: false,
      hide: false
    }
  },
  onLoad () {
    this.init = true
    // let phoneInfo = wx.getStorageSync('phoneInfo')
    let phoneInfo = this.globalData.deviceInfo || wx.getSystemInfoSync()
    console.log('navigate load phoneInfo:', phoneInfo)
    if (phoneInfo.version >= '7.0.0') {
      this.hide = false
      this.statusBarHeight = phoneInfo.statusBarHeight
      if (phoneInfo.system.indexOf('iOS') === -1) {
        this.isIOS = false
      }
    } else {
      this.hide = true
    }
  },
  onReady () {
  },
  onUnload () {
  },
  methods: {
    backPage () {
      wx.navigateBack({
        delta: 1
      })
    },
    toHome () {
      if (this.callbackFun === true) {
        this.$emit('onHomeBtnClickHander')
      } else {
        wx.reLaunch({
          url: '/pages/main/main'
        })
      }
    }
  },
  components: {

  }
}
</script>

<style scoped lang="css">
.navigate-container {
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 9999;
  /* background: linear-gradient(90deg,rgba(176,110,39,.6),rgba(239,213,164,1),rgba(219,183,116,1)); */
}
.navigate-bar {
  width: 100%;
  display: flex;
}
.isIOS {
  justify-content: space-around;
}
.navigate-icon {
  width: 80rpx;
  box-sizing: border-box;
  padding-left: 18rpx;
  display: flex;
  align-items: center;
  position: absolute;
  left: 0rpx;
}
.navigate-title {
  text-align: center;
  line-height: 90rpx;
  font-size: 33rpx;
  text-overflow: ellipsis;
  overflow: hidden;
  white-space: nowrap;
}
.androidTitle {
  /* position: relative; */
  /* left: 90rpx; */
  margin-left: 90rpx;
  font-size: 38rpx;
  line-height: 100rpx;
}
.navigator-back {
  height: 100%;
  width: 100%;
  align-items: center;
  justify-content: center;
  display: flex;
  position: relative;
  top: 5rpx;
}

.navigator-hover {
  background-color: rgba(0, 0, 0, 0.1);
  opacity: 0.7;
}
.navigate-bar.isIOS .navigate-icon.navigator-hover {
  background-color: transparent;
  opacity: 1;
}
.icon-home {
  font-size: 42rpx;
}
.icon-back4 {
  font-size: 34rpx;
}
</style>
