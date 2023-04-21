<template>

  <div class="black-bg" v-if="modal == true">
    <div class="white-bg">
      <h4>상세페이지</h4>
      <p>상세페이지 내용</p>
      <button @click="modal = false">닫기</button>
    </div>
  </div>

  <div class = "menu">
    <a v-for="a in menu" :key="a">{{ a }}</a>
  </div>

  <div v-for="(a,i) in 3" :key="i">
    <img :src="require('./assets/room' + i + '.jpg')" class = "room-img">
    <h4 @click="modal = true">{{ products[i] }}</h4>
    <p>{{ price[i] }}만원</p>
    <button @click="increase(i)">허위매물 신고</button> <span>신고수: {{신고수[i]}} </span>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      modal : false,
      신고수 : [0, 0, 0], 
      menu: ['Home', 'Shop', 'About'],
      products : ['역삼동 원룸', '천호동 원룸', '마포구 원룸'],
      price : ['60', '70', '80'],
      스타일: 'color : darkslateblue',
    }
  },
  methods : {
    increase(id){
      this.신고수[id] += 1;
    }
  },
  components: {
  }
}
</script>

<style>
body {
  margin : 0;
}
div {
  box-sizing: border-box;
}
.black-bg {
  width: 100%; height:100%;
  background: rgba(0,0,0,0.5);
  position: fixed; padding: 20px;
}
.white-bg {
  width: 100%; background: white;
  border-radius: 8px;
  padding: 20px;
} 

.room-img{
  width: 100%;
  margin-top:  40px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu{
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}

.menu a{
  color: white;
  padding: 10px;
}

</style>
