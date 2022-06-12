<template>
  <div class="container">
    <div class="squares">
      <div class="content d-flex flex-column justify-content-between">
        <div class="d-flex justify-content-between">
          <div
            @click="clickMethod($event)"
            style="background: #264653"
            class="square"
          ></div>
          <div style="background: #2a9d8f" class="square"></div>
        </div>
        <div class="gridd d-flex align-self-center">central grid</div>
        <div class="d-flex justify-content-between">
          <div style="background: #f4a261" class="square"></div>
          <div style="background: #e76f51" class="square"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    clickMethod(event) {
      console.log(event.target.style.background);
    },
  },
};
</script>
=

<style lang="css" scoped>
html,
body {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
}

.container {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.squares {
  position: relative;
  width: 80vmin;
  border: solid red 5px;
  box-sizing: border-box;
}

.square {
  cursor: pointer;
  width: 100px;
  height: 100px;
  background: rgb(246, 156, 85);
}
</style>
