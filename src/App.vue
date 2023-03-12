<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div>
    <h4 :style="스타일">{{ products[0] }}</h4> 
    <p>{{ price1 }} 만원</p>
  </div>
  <div>
    <h4 :style="스타일">{{ products[1] }}</h4>
    <p>{{ price2 }} 만원</p>
  </div>
  <div>
    <h4 :style="스타일">{{ products[2] }}</h4>
    <p>{{ price3 }} 만원</p>
  </div>
</template>

<script>


export default {
  name: 'App',
  data(){
    return {
      price1 : 60,
      price2 : 70,
      price3 : 80,
      products : ['역삼동 원룸', '천호동 원룸', '마포구 원룸'],
      스타일: 'color : #00008B',
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
  margin-top: 60px;
}
</style>
