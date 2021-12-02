<template>
  <div>
    <button v-on:click="shuffle">Shuffle</button>
    <transition-group name="flip-list" tag="div" class="grid">
      <template v-for="item in items">
        <div :key="item" :class="'a' + item">
          {{ item }}
        </div>
      </template>
    </transition-group>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data() {
    return {
      items: [1, 2, 3, 4, 5, 6, 7, 8, 9],
    }
  },
  methods: {
    shuffle: function () {
      const shuffle_ = function (array: any[]) {
        var currentIndex = array.length,
          temporaryValue,
          randomIndex

        // While there remain elements to shuffle...
        while (0 !== currentIndex) {
          // Pick a remaining element...
          randomIndex = Math.floor(Math.random() * currentIndex)
          currentIndex -= 1

          // And swap it with the current element.
          temporaryValue = array[currentIndex]
          array[currentIndex] = array[randomIndex]
          array[randomIndex] = temporaryValue
        }

        return array
      }
      let a = this.items
      this.items = []
      this.items = shuffle_(a)
      console.log(this.items)
    },
  },
})
</script>

<style>
.flip-list-move {
  transition: transform 1s;
}
</style>