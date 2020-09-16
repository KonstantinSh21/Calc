<template>
  <div class="wrapper">
    <div class="wrapper-calc">
      <Display
          v-bind:numberOne="numberOne"
          v-bind:action="action"
          v-bind:numberTwo="numberTwo"
      />
      <Number
          v-on:one="one"
          v-on:two="two"
          v-on:plus="plus"

          v-on:final="final"
      />
    </div>

  </div>
</template>
<script>

import Display from "@/components/Display/Display";
import Number from "@/components/Number/Number"

export default {
  name: "Layout",
  components:{
    Display,
    Number
  },
  data(){
    return{
      numberOne: 0,
      numberTwo: null,
      action: '',
      result: '',
    }
  },
  methods:{

    one(e){
      console.log(e)
      this.numberOne = this.numberOne + toString(e)
      this.numberOne += this.numberOne

      console.log(typeof this.numberOne)
    },
    two(e){
      if(this.action === ''){
        this.numberOne = this.numberOne + e
      } else {
        this.numberTwo = this.numberTwo + e
      }
    },

    plus(e){
      this.action = e
    },

    final(){
      console.log(typeof this.numberTwo)
      // this.result = this.numberOne + this.numberTwo
      this.numberOne = Number(this.numberOne)
      console.log(typeof this.numberTwo)
      // console.log(this.result)
    }



  }
}
</script>

<style scoped>
.wrapper{
  position: relative;
  padding-top: 50px ;
  width: 100%;
}
.wrapper-calc{
  text-align: center;
  margin: 0 auto;
  width: 40%;
  background-color: #ccc;
}


</style>