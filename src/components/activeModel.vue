<template>
  <div class="model_box container_flex column center pingmucenter"
       :class="{'active': showActive}"
       :style="{ height: aheight +'rpx', width: awidth +'rpx' }">
    <slot></slot>
  </div>
</template>
<script>
export default {
  props: ['showActive', 'aheight', 'awidth'],
  data () {
    return {
    }
  },
  methods: {
  },
  onload () {

  }
}
</script>
<style scoped lang="less">
.model_box {
  position: absolute;
  top: 5%;
  left: 10%;
  width: 80%;
  height: 80%;
  opacity: 1;
  overflow-y: scroll;
  border-radius: 30rpx;
  transform: scale(1);
  transition: all 0.3s;
  background-color: #fff;
}
.active {
  transform: scale(1);
  opacity: 1;
}
</style>
