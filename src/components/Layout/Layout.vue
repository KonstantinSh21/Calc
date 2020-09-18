<template>
  <div class="wrapper">
    <div class="wrapper-calc">
      <Display
          v-bind:numberOne="numberOne"
          v-bind:action="action"
          v-bind:numberTwo="numberTwo"
          v-bind:result="result"
          v-bind:showResult="showResult"
      />
      <Number
          v-on:num="num"

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
  components: {
    Display,
    Number
  },
  data() {
    return {
      numberOne: '',
      numberTwo: '',
      action: '',
      result: 0,

      showResult: false,
    }
  },
  methods: {
    num(e) {
      this.showResult = false
      this.result = 0
      if (this.action === '') {
        this.numberOne += e
      } else {
        this.numberTwo += e
      }

    },
    plus(e) {
      if(this.numberOne !== ""){
        this.action = e
      }


    },

    final() {

      if(this.numberOne !== "" && this.numberTwo !== ""){
        this.showResult = true
        console.log(this.action)
        if(this.action === "+"){
          this.result = +this.numberOne + +this.numberTwo
          console.log(this.result)
        }
        if(this.action === "-"){
          this.result = +this.numberOne - +this.numberTwo
          console.log(this.result)
        }
        if(this.action === "*"){
          this.result = +this.numberOne * +this.numberTwo
          console.log(this.result)
        }
        if(this.action === "/"){
          this.result = +this.numberOne / +this.numberTwo
          console.log(this.result)
        }
        this.numberOne = ''
        this.numberTwo = ''
        this.action = ''
      }

    }


  }
}
</script>

<style scoped>
.wrapper {
  position: relative;
  padding-top: 50px;
  width: 100%;
}

.wrapper-calc {
  text-align: center;
  margin: 0 auto;
  width: 30%;
  background-color: #ccc;
}


</style>