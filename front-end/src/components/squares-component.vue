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
          <div
            @click="clickMethod($event)"
            style="background: #2a9d8f"
            class="square"
          ></div>
        </div>
        <div class="d-flex justify-content-center">
          <GridComponent
            :selectedColors="selectedColors"
            @RemoveColorFromArray="RemoveColorFromArray"
          ></GridComponent>
        </div>

        <div class="d-flex justify-content-between">
          <div
            @click="clickMethod($event)"
            style="background: #f4a261"
            class="square"
          ></div>
          <div
            @click="clickMethod($event)"
            style="background: #e76f51"
            class="square"
          ></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import GridComponent from "./grid-component.vue";
export default {
  components: {
    GridComponent,
  },
  name: "SquaresComponent",
  data() {
    return {
      selectedColors: [],
    };
  },
  methods: {
    clickMethod(event) {
      this.selectedColors.push(event.target.style.background);

      console.log("before:", this.selectedColors);
    },
    removeItem(array, item) {
      for (let i = 0; i < array.length; i++) {
        if (array[i] == item) {
          array.splice(array.indexOf(item), 1);
          i--;
        }
      }
    },

    RemoveColorFromArray(el) {
      this.removeItem(this.selectedColors, el);
      console.log("rrrrrrr:", this.selectedColors);
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
