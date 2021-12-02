<template>
  <div class="right">
    <MenuItem class="menu-item">
      <template v-slot:label>ไทย</template>
    </MenuItem>
    <div>|</div>
    <MenuItem class="menu-item">
      <template v-slot:label>EN</template>
    </MenuItem>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import MenuItem from './MenuItem.vue'

export default Vue.extend({
  components: {
    MenuItem,
  },
})
</script>

<style scoped lang="scss">
.right {
  display: flex;
  justify-content: space-between;
  align-items: center;
  > div {
    margin-left: 25px;
    color: #717171;
  }
  .menu-item:hover {
    cursor: pointer;
    color: #303030;
  }
}
</style>