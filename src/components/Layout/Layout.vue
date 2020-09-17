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
          v-on:one="one"
          v-on:two="two"
          v-on:three="three"
          v-on:four="four"
          v-on:five="five"
          v-on:six="six"
          v-on:seven="seven"
          v-on:eight="eight"
          v-on:nine="nine"
          v-on:zero="zero"

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


    one(e) {
      this.showResult = false
      this.result = 0
      // console.log(typeof this.numberOne)
      if (this.action === '') {
        this.numberOne += e
      } else {
        this.numberTwo += e
      }

    },

    two(e) {
      this.showResult = false
      this.result = 0
      if (this.action === '') {
        this.numberOne += e
      } else {
        this.numberTwo += e
      }
    },
    three(e) {
      this.showResult = false
      this.result = 0
      if (this.action === '') {
        this.numberOne += e
      } else {
        this.numberTwo += e
      }
    },
    four(e) {
      this.showResult = false
      this.result = 0
      if (this.action === '') {
        this.numberOne += e
      } else {
        this.numberTwo += e
      }
    },
    five(e) {
      this.showResult = false
      this.result = 0
      if (this.action === '') {
        this.numberOne += e
      } else {
        this.numberTwo += e
      }
    },
    seven(e) {
      this.showResult = false
      this.result = 0
      if (this.action === '') {
        this.numberOne += e
      } else {
        this.numberTwo += e
      }
    },
    eight(e) {
      this.showResult = false
      this.result = 0
      if (this.action === '') {
        this.numberOne += e
      } else {
        this.numberTwo += e
      }
    },
    nine(e) {
      this.showResult = false
      this.result = 0
      if (this.action === '') {
        this.numberOne += e
      } else {
        this.numberTwo += e
      }
    },
    six(e) {
      this.showResult = false
      this.result = 0
      if (this.action === '') {
        this.numberOne += e
      } else {
        this.numberTwo += e
      }
    },
    zero(e) {
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
  width: 40%;
  background-color: #ccc;
}


</style>