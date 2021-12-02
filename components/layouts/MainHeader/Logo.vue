<template>
  <div class="logo-container">
    <div class="logo">
      <img src="~/assets/images/logo.png" alt="" />
    </div>
    <div class="text">
      <div class="text">KOFE</div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({})
</script>

<style scoped lang="scss">
.logo-container {
  display: flex;
  align-items: center;
  margin-right: 15px;
  > .logo {
    display: flex;
    align-items: center;
    margin-right: 10px;
    height: 100%;
    > img {
      height: 50px;
    }
  }
  > .text {
    color: #BD5663;
    height: 100%;
    font-size: 1.4em;
  }
}
</style>