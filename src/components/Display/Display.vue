<template>
  <div class="wrapper-display">
    <div class="display">
      <div class="display-number">
        {{numberOne}} {{action}} {{numberTwo}} {{result}}
      </div>
    </div>
  </div>
</template>
<script>

export default {
  name: "Display",
  props:["numberOne", "action", "numberTwo", "result"]
}
</script>

<style>
.wrapper-display {

  min-width: 100%;
  height: 100px;
}

.display {
  text-align: left;
  height: 100px;
  padding-top: 10px;
  padding-left: 10px;

}
.display-number{
  height: 50px;
  margin-left: 40px;
  margin-top: 30px;
  max-width: calc(87% + 2px);
  font-size: 40px;
  background-color: #888;
}

</style>