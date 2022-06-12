<template>
  <div class="d-flex flex-wrap justify-content-between">
    <div class="square"></div>
    <div class="square"></div>
    <div class="square"></div>
    <div class="square"></div>
    <div class="square"></div>
    <div class="square"></div>
    <div class="square"></div>
    <div class="square"></div>
    <div class="square"></div>
    <div class="square"></div>
  </div>
</template>

<script>
export default {
  name: "GridComponent",
};
</script>

<style lang="css" scoped>
.square {
  cursor: pointer;
  width: 100px;
  height: 100px;
  background: rgb(246, 156, 85);
  flex-basis: 33.333333%;
  border: solid black 3px;
  margin: 0 auto;
}
</style>
