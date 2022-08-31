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
      <div class="test_box">
        关于我们
        <br>
        -----------------------
        <br> 
        本次实践活动延续红色翻译团队之前对南京景点的考察，将区域进一步扩大，辐射到北京和上海地区。
        <br>
        考虑到以更多、更好的方式进行宣传，使我们的实践成果能够产生更大范围的良性影响，我们在“九乡河翻译专业团队”微信公众号之外，又新增了本次的红色翻译微信小程序。
        <br>
        我们的小程序主要是一张文化地图，集中于南京区域，选取“中山陵”、“侵华日军南京大屠杀遇难同胞纪念馆”、“南京博物院”、“南京云锦博物馆”、“南京渡江胜利纪念馆”、“总统府”这六个具有代表性的文化景点，这些景点不仅文化历史底蕴丰富，而且属于爱国主义教育基地，其中还包括了几个地处南京的全国爱国主义教育示范基地。
        <br>
      </div>
      <!-- 这里自定义所需的弹框内容-->
    </div>
  </activeModel>
</mask>

    
    <button class="button" @click="showTestMask()"> 关于我们 </button>
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
        nickName: '译旅金陵·南京爱国主义教育基地双语地图',
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
.test_box {
  text-align: center;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  font-size: medium;
}
.tot_background {
  
  width: 100%;
  height: 600px;
  background-size: 100% 100%;
  background-image: url(https://636c-cloud1-5gvc6j32238c5e8b-1313536818.tcb.qcloud.la/background2.jpeg?sign=54a8281517343bf2d034fa0e75acba8e&t=1661945795);
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
  font-family: 'Times New Roman', Times, serif;
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
   top: 300px;
   background-color: rgb(66, 66, 81);
   color: white;
   border-block-color: red;
   border-block-width: 10px;
   padding-left: 10px;
   padding-right: 10px;
   border-radius: 100px;
   font-weight: 700;
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
