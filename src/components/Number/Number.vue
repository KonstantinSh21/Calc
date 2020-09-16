<template>
  <div class="wrapper-num">
    <div v-on:click="$emit('one', 1)" class="num">1</div>
    <div v-on:click="$emit('two', 2)" class="num">2</div>
    <div v-on:click="$emit('three', 3)" class="num">3</div>
    <div v-on:click="$emit('plus', '+')" class="num">+</div>
    <div v-on:click="$emit('minus', '-')" class="num">-</div>
    <div v-on:click="$emit('four', 4)" class="num">4</div>
    <div v-on:click="$emit('five', 5)" class="num">5</div>
    <div v-on:click="$emit('six', 6)" class="num">6</div>
    <div v-on:click="$emit('multiply', '*')" class="num">x</div>
    <div v-on:click="$emit('share', '/')" class="num">/</div>
    <div v-on:click="$emit('seven', 7)" class="num">7</div>
    <div v-on:click="$emit('eight', 8)" class="num">8</div>
    <div v-on:click="$emit('nine', 9)" class="num">9</div>
    <div v-on:click="$emit('final')" class="asd">=</div>
  </div>
</template>
<script>
export default {
  name:"Number",

}
</script>

<style>
.wrapper-num{
  padding-top: 40px;
  background-color: #888;
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  padding-bottom: 10px;
}
.num{
  flex: 1 1 20%;
  height: 40px;
}
.asd{
  flex: 1 1 40%;
}



</style>