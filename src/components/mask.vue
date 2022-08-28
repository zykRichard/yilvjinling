<template>
  <div v-if="isShow"
       catchtouchmove="ture"
       class="mask"
       :class="{'active': showBgk}"
       :style="{top:top+'rpx'}"
       id="mask"
       @click="hideMask($event)">
    <slot></slot>
  </div>
</template>
<script>
export default {
  props: ['top', 'bgcolor', 'noclickhide'],
  data () {
    return {
      isShow: false,
      showBgk: false
    }
  },
  onLoad () {
    this.isShow = false
    console.log('00')
  },
  methods: {
    hideMask (e) {
      if (!e) {
        this.toHideMask()
      } else if (e.target.id === 'mask') {
        if (this.noclickhide) return // msak 点击屏蔽
        this.toHideMask()
      }
    },
    showMask () {
      this.showBGK()
      this.$emit('onShowHander')
    },
    toHideMask () {
      this.hideBGK()
      this.$emit('onHideHander')
    },
    showBGK () {
      this.isShow = true
      let _this = this
      setTimeout(() => {
        _this.showBgk = true
      }, 100)
    },
    hideBGK () {
      let _this = this
      setTimeout(() => {
        this.showBgk = false
        setTimeout(() => {
          _this.isShow = false
        }, 200)
      }, 100)
    }
  }
}
</script>
<style scoped lang="less">
.mask {
  width: 100%;
  height: 100%;
  position: fixed;
  left: 0;
  z-index: 999;
  opacity: 0;
  transition: all 0.2s;
}
.active {
  opacity: 1;
  background-color: rgba(0, 0, 0, 0.5);
}
</style>