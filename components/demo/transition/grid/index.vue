<template>
  <div>
    <div class="grid-wrapper">
      <div class="grid">
        <div v-for="block in blocks" :key="block" :class="'a' + block" :ref="'item' + block">
          {{ block }}
        </div>
        <div class="items"></div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  data() {
    return {
      blocks: [1, 2, 3, 4],
    }
  },
})
</script>

<style scoped lang="scss">
.items {
  position: absolute;
  width: 100%;
  height: 100%;
}
.item1 {
  background-color: rgb(255, 153, 153);
}
.item2 {
  background-color: rgb(255, 243, 136);
}
.item3 {
  background-color: rgb(146, 255, 119);
}
.item4 {
  background-color: rgb(102, 255, 235);
}
.grid-wrapper {
  height: 400px;
  width: 800px;
  background-color: #ddd;
}
.a1 {
  grid-area: a1;
}
.a2 {
  grid-area: a2;
}
.a3 {
  grid-area: a3;
}
.a4 {
  grid-area: a4;
}
.grid {
  position: relative;
  width: 100%;
  height: 100%;
  display: grid;
  grid-template:
    'a1 a1 a1'
    'a2 a3 a4';
  > div {
    border: 1px #111 solid;
  }
}
</style>