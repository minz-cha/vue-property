<template>

  <div class = "menu">

    <!-- 반복문: 'v-for="작명 in 몇회" :key=""' 
    반복문 쓸 때 ':key="작명"' 안쓰면 에러남 -->
    <a v-for="a in menu" :key="a">{{ a }}</a>
    <!-- 'v-for="(a,i) in 메뉴들" :key="i"'
    처럼 변수 작명 2개까지 가능 - 왼쪽변수: array내의 데이터, 오른쪽변수: 1씩 증가하는 함수 -->

  </div>

  <div v-for="(a,i) in 3" :key="i">
    <h4>{{ products[i] }}</h4>
    <p>{{ price[i] }}만원</p>
  </div>
  <!-- <div>
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
  </div> -->
</template>

<script>


export default {
  name: 'App',
  data(){
    return {
      price1 : 60,
      price2 : 70,
      price3 : 80,
      menu: ['Home', 'Shop', 'About'],
      products : ['역삼동 원룸', '천호동 원룸', '마포구 원룸'],
      price : ['60', '70', '80'],
      스타일: 'color : darkslateblue',
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
