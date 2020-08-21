<template>
  <div id="example-1">
    <!--<button @click="upFunction()" class="btn btn-info">{{label}}</button>-->
    <button @click="LikeFunction()" class="btn btn-info">
      <i class='far fa-smile-wink' style='font-size:28px;color:black'></i>
    </button>
    <button @click="LoveFunction()" class="btn btn-danger">
      <i class='far fa-kiss-wink-heart' style='font-size:28px;color:black'></i>
      </button>
    <button @click="HahaFunction()" class="btn btn-warning">
      <i class='far fa-laugh-beam' style='font-size:28px;color:Black'></i>
    </button>
    <button @click="WowFunction()" class="btn btn-success">
      <i class='far fa-dizzy' style='font-size:28px;color:black'></i>
      </button>
    <button @click="SadFunction()" class="btn btn-info">
      <i class='far fa-sad-cry' style='font-size:28px;color:black'></i>
      </button>
    <button @click="AngryFunction()" class="btn btn-danger">
      <i class='far fa-grimace' style='font-size:28px;color:black'></i>
      </button>
    <p v-bind:style="{fontSize: fsize + 'px' }"> {{ counter }} </p>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      counter: 0,
    }
  },
  methods:{
    LikeFunction: function(){
      this.counter += 1
      //1.ส่งค่าตัวแปร counter ออกไปโดยผ่านตัวแปร cc
      this.$emit('cc',this.counter)

    },
    LoveFunction: function(){
      this.counter += 10
      this.$emit("cc", this.counter);
    },
    HahaFunction: function(){
      this.counter += 5
      this.$emit("cc", this.counter);
    },
    WowFunction: function(){
      this.counter += 20
      this.$emit("cc", this.counter);
    },
    SadFunction: function(){
      this.counter -= 5
      this.$emit("cc", this.counter);
    },
    AngryFunction: function(){
      this.counter -= 50
      this.$emit("cc", this.counter);
    },
    ResetFunction: function () {
      this.counter = 0;
      this.$emit("cc", this.counter);
    },
    sum(counterValue){
      this.total += counterValue
    },
  },
  props: {
    label: String
  },
};
</script>

<style>
</style>

