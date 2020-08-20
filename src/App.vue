<template>
  <div id="app">
    <h1>Nut Nutthapon Pandeang</h1>
    <div id="myCarousel" class="carousel slide" data-ride="carousel">
    <ol class="carousel-indicators" >
      <li data-target="#myCarousel" data-slide-to="0" class=""></li>
      <li data-target="#myCarousel" data-slide-to="1" class="active"></li>
      <li data-target="#myCarousel" data-slide-to="2" class=""></li>
    </ol>
    <div class="carousel-inner">
      <div class="carousel-item">
        <img src="./assets/P1.jpg" class="bd-placeholder-img bd-placeholder-img-lg featurette-image img-fluid mx-auto" width="500" height="500" preserveAspectRatio="xMidYMid slice" focusable="false" role="img" alt="" srcset="" aria-label="Placeholder: 500x500">
      </div>
      <div class="carousel-item active">
        <img src="./assets/P2.jpg" class="bd-placeholder-img bd-placeholder-img-lg featurette-image img-fluid mx-auto" width="500" height="500" preserveAspectRatio="xMidYMid slice" focusable="false" role="img" alt="" srcset="" aria-label="Placeholder: 500x500">
      </div>
      <div class="carousel-item">
        <img src="./assets/P3.jpg" class="bd-placeholder-img bd-placeholder-img-lg featurette-image img-fluid mx-auto" width="500" height="500" preserveAspectRatio="xMidYMid slice" focusable="false" role="img" alt="" srcset="" aria-label="Placeholder: 500x500">
      </div>
    </div>
  </div>
    <HelloWorld msg="" />
    <div class="row">
      <div class="col-12">
        <!-- 2.รับค่าจาก emit @cc แล้วส่งไปทำงานใน function "sum"-->
        <like label="" @cc = "sum" />
      </div>
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Like from "./components/Like.vue";
export default {
  name: "App",
  components: {
    HelloWorld,
    Like,
  },
    props: {
    label: String
  },
}


</script>

<style>
#app {
  font-family: 'Do Hyeon', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ffffff;
  margin-top: 60px;
}
body{
  background-image: url("./assets/BG02.png");
}
</style>
