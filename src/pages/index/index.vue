<template>
  <div class="tot_background" @click="clickHandle" >
   

    <div class="userinfo" @click="bindViewTap">
      <!-- <img class="userinfo-avatar" v-if="userInfo.avatarUrl" :src="userInfo.avatarUrl" background-size="cover" /> -->
      <img class="userinfo-avatar" src="/static/images/logo.jpeg" background-size="cover" />

      <div class="userinfo-nickname">
        <card :text="userInfo.nickName"></card>
      </div>
    </div>

    <!-- <div class="usermotto">
      <div class="user-motto">
        <card :text="motto"></card>
      </div>
    </div> -->

    <!-- 弹窗部分 -->
    <div class="header-box"
         :style="{top: '100px'}">
      <mask ref="testMask"
            top="0" 
      :noclickhide='false'
      @onHideHander="onHideTestMask()"
      @onShowHander="onShowTestMask()">
  <activeModel :showActive="showActive" >
    <div>
      <div class="test_box"> 加入引言 </div>
      <!-- 这里自定义所需的弹框内容-->
    </div>
  </activeModel>
</mask>

    
    <button class="button" @click="showTestMask()"> aboutus </button>
    </div>
  </div>
</template>

<script>
import card from '@/components/card'
import activeModel from '@/components/activeModel'
import mask from '@/components/mask'
export default {
  data () {
    return {
      motto: 'Hello ',
      userInfo: {
        nickName: '这是标题',
        avatarUrl: 'http://mpvue.com/assets/logo.png'
      },
      showActive: true
    }
  },

  components: {
    card, mask, activeModel
  },

  methods: {
    showTestMask () {
      this.$refs.testMask.showMask()
    },
    onHideTestMask () {
      this.showActive = false
    },
    onShowTestMask () {
      let _this = this
      setTimeout(() => {
        console.log('>>>>>>>', _this.showActive)
        _this.showActive = true
        console.log('>>>>>>>', _this.showActive)
      }, 100)
    },
    bindViewTap () {
      const url = '../logs/main'
      if (mpvuePlatform === 'wx') {
        mpvue.switchTab({ url })
      } else {
        mpvue.navigateTo({ url })
      }
    },
    clickHandle (ev) {
      console.log('clickHandle:', ev)
      // throw {message: 'custom test'}
    }
  },
  created () {
    // let app = getApp()
  }
}
</script>

<style scoped>
page {
  height: 700px;
}
.tot_background {
  
  width: 100%;
  height: 600px;
  background-size: 100% 100%;
  background-image: url(https://636c-cloud1-5gvc6j32238c5e8b-1313536818.tcb.qcloud.la/background.jpg?sign=4aff421c151b069d5097f256b4ccf6f7&t=1661702012);
} 
.userinfo {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.userinfo-avatar {
  position: relative;
  width: 300rpx;
  height: 300rpx;
  margin: 20rpx;
  top: 20rpx;
  border-radius: 50%;
}

.userinfo-nickname {
  position: relative;
  top: 10rpx;
  color: rgb(135, 10, 116);
  font-family:Georgia, 'Times New Roman', Times, serif;
}

.usermotto {
  position: relative; 
  margin-top: 300px;
}
/* .test_box {
  position: absolute;
  width: 560rpx;
  height: 368rpx;
  opacity: 1;
  transform: scale(0.5);
  border-radius: 30rpx;
  transition: all 0.3s;
  background-color: white;
} */
.button {
   position: relative;
   width: 50%;
   display: block;
   top: 200px;
   background-color: rgb(131, 160, 79);
   color: white;
   border-block-color: red;
   border-block-width: 10px;
   padding-left: 10px;
   padding-right: 10px;
   border-radius: 100px;
}
.form-control {
  display: block;
  padding: 0 12px;
  margin-bottom: 5px;
  border: 1px solid #ccc;
}
.all{
  width:7.5rem;
  height:1rem;
  background-color:blue;
}
.all:after{
  display:block;
  content:'';
  clear:both;
}
.left{
  float:left;
  width:3rem;
  height:1rem;
  background-color:red;
}

.right{
  float:left;
  width:4.5rem;
  height:1rem;
  background-color:green;
}
</style>
