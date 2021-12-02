<template>
  <div class="left">
    <template v-for="item in items">
      <MenuItem class="menu-item" :key="item">
        <template v-slot:label>Menu {{ item }}</template>
      </MenuItem>
    </template>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import MenuItem from './MenuItem.vue'
export default Vue.extend({
  data() {
    return {
      items: [1, 2, 3, 4, 5],
    }
  },
  components: {
    MenuItem,
  },
})
</script>

<style scoped lang="scss">
.left {
  display: flex;
  justify-content: space-between;
  align-items: center;
  > div {
    margin-right: 55px;
    color: #717171;
  }
  .menu-item:hover {
    cursor: pointer;
    color: #303030;
  }
}
</style>