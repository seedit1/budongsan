<template>
  <div class="menu">
    <a v-for="a in 메뉴들" :key="a">{{a}}</a>    
  </div> 
  <div>
    <h4>{{products[0]}}</h4>
    <p>{{price1[0]}}만원</p>
    <button @click=increase1>허위매물신고</button>
    <span>신고수 : {{신고수[0]}}</span> 
  </div>
  <div>
    <h4>{{products[1]}}</h4>
    <p>{{price1[1]}}만원</p> 
    <button @click=increase2>허위매물신고</button><span>신고수 : {{신고수[1]}}</span>
  </div>  
  <div>
    <h4>{{products[2]}}</h4>
    <p>{{price1[2]}}만원</p>
    <button @click=increase3>허위매물신고</button><span>신고수 : {{신고수[2]}}</span> 
  </div>      
</template>

<script>


export default {
  name: 'App',
  data(){
    return {
      price1:[ 60, 70, 80 ],      
      메뉴들 : ['Home', 'Shop', 'About'],
      products : ['역삼동 원룸', '천호동 원룸', '마포구 원룸'],
      신고수: [0, 0, 0,],     
    }
  },
  methods: {
    increase1(){
      this.신고수[0]++;
    },
    increase2(){
      this.신고수[1]++;
    },
    increase3(){
      this.신고수[2]++;
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
.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;  
}
.menu a {
  color : white;
  padding: 10px;
}
</style>
