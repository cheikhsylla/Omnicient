<template>
  <div class="d-flex flex-wrap justify-content-between">
    <div
      class="square"
      v-for="square in numberOfGrid"
      :key="square"
      v-bind:style="{ background: selectedColors[square] }"
      @click="RemoveColorFromArray($event)"
    >
      {{ square }}
    </div>
  </div>
</template>

<script>
export default {
  name: "GridComponent",
  props: {
    selectedColors: {
      type: Array,
    },
  },
  data() {
    return {
      numberOfGrid: 10,
    };
  },
  methods: {
    RemoveColorFromArray(event) {
      this.$emit("RemoveColorFromArray", event.target.style.background);
    },
  },
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
