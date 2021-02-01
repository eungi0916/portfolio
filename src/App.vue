<template>
  <div>
  <h1>Hello {{ animal}}</h1>
  <h2>원숭이는 {{food}} 를 좋아한다.</h2>
  <h3> </h3>
  <input type="text" v-model="food"> 
  <div v-html="alertMesaage"></div>
  <div v-html="subscribeHTML"></div>
  <img v-bind:src="imageSource" alt="random">
  <a :href="food">{{food}}</a>
  </div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      animal: "Monkey",
      food: "apple",
      alertMesaage: "<h2>경고</h2>",
      subscribeHTML: `<button onclick="document.querySelector('body').style.display ='none'">구독하기</button>`,
      imageSource: "https://placeimg.com/100/100/any",
      naverUrl: "https://www.naver.com",
    }
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
input {
  font-size: 20px;
}
</style>
