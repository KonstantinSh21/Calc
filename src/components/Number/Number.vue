<template>
  <div class="wrapper-num">
    <div v-on:click="$emit('num', 1)" class="num"><span>1</span></div>
    <div v-on:click="$emit('num', 2)" class="num"><span>2</span></div>
    <div v-on:click="$emit('num', 3)" class="num"><span>3</span></div>
    <div v-on:click="$emit('plus', '+')" class="num"><span>+</span></div>
    <div v-on:click="$emit('plus', '-')" class="num"><span>-</span></div>
    <div v-on:click="$emit('num', 4)" class="num"><span>4</span></div>
    <div v-on:click="$emit('num', 5)" class="num"><span>5</span></div>
    <div v-on:click="$emit('num', 6)" class="num"><span>6</span></div>
    <div v-on:click="$emit('plus', '*')" class="num"><span>*</span></div>
    <div v-on:click="$emit('plus', '/')" class="num"><span>/</span></div>
    <div v-on:click="$emit('num', 7)" class="num"><span>7</span></div>
    <div v-on:click="$emit('num', 8)" class="num"><span>8</span></div>
    <div v-on:click="$emit('num', 9)" class="num"><span>9</span></div>
    <div v-on:click="$emit('num', 0)" class="num"><span>0</span></div>
    <div v-on:click="$emit('final')" class="num"><span>=</span></div>
  </div>
</template>
<script>
export default {
  name:"Number",

}
</script>

<style>
.wrapper-num{
  padding-top: 10px;
  background-color: #888;
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  padding-bottom: 10px;
}
.num{
  flex: 1 1 15%;
  height: 40px;
  background-color: #999;
  margin: 10px;
  border-radius: 100%;
  cursor: pointer;
}
.num span{
  display: block;
  padding-top: 5px;
  margin: auto 0;
  font-size: 22px;
}



</style>