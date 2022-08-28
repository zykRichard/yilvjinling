<template>
  <div class='map'>
    <button class="btn" @click="aclick">.</button>
    <button class="btn" @click="bclick">.</button>
    <button class="btn" @click="cclick">.</button>
    <button class="btn" @click="dclick">.</button>
    <button class="btn" @click="eclick">.</button>
    <button class="btn" @click="fclick">.</button>
  </div>
</template>

<script>
export default {
  name: 'map',
  methods: {
    aclick () {
      // console.log(URL('/static/images/南京博物院.png'))
      console.log('南京博物院')
      console.log('content')
    },
    bclick () {
      console.log(URL('/static/images/总统府.png'))
      console.log('总统府')
      console.log('content')
    },

    cclick () {
      console.log(URL('/static/images/中山陵.png'))
      console.log('中山陵')
      console.log('content')
    },

    dclick () {
      console.log(URL('/static/images/渡江胜利纪念馆.png'))
      console.log('渡江胜利纪念馆')
      console.log('content')
    },

    eclick () {
      console.log(URL('/static/images/南京大屠杀遇难同胞纪念馆.png'))
      console.log('南京大屠杀遇难同胞纪念馆')
      console.log('content')
    },

    fclick () {
      console.log(URL('/static/images/南京云锦博物馆.png'))
      console.log('南京云锦博物馆')
      console.log('content')
    }
  }
}
</script>

<style>
page {
  height: 100%;
  text-align: center;
}

.btn {
  border-radius:100%;
  backgrounkcolor: #4CAF50;
  font-color: #4CAF50;
}
