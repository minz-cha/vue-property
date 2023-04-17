<template>

  <div class = "menu">
    <a v-for="a in menu" :key="a">{{ a }}</a>
  </div>

  <div v-for="(a,i) in 3" :key="i">
    <h4>{{ products[i] }}</h4>
    <p>{{ price[i] }}만원</p>
    <button @click="increase(i)">허위매물 신고</button> <span>신고수: {{신고수[i]}} </span>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      신고수 : [0, 0, 0], 
      price1 : 60,
      price2 : 70,
      price3 : 80,
      menu: ['Home', 'Shop', 'About'],
      products : ['역삼동 원룸', '천호동 원룸', '마포구 원룸'],
      price : ['60', '70', '80'],
      스타일: 'color : darkslateblue',
    }
  },
  // vue에서 함수 생성
  // methods : { 함수(){} }
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
