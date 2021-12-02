<template>
  <div class="input-wrapper">
    <input class="input" type="text" placeholder="Placeholder" />
    <!-- <div class="icon-start">S</div> -->
    <div class="icon-end">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="24"
        height="24"
        viewBox="0 0 24 24"
        fill="none"
        stroke="currentColor"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
        class="feather feather-search"
      >
        <circle cx="11" cy="11" r="8"></circle>
        <line x1="21" y1="21" x2="16.65" y2="16.65"></line>
      </svg>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style scoped lang="scss">
.input-wrapper {
  height: 44px;
  width: 100%;
  position: relative;
  .input {
    background-color: var(--search-box-bg, white);
    border: 1px solid #dfdfdf;
    border-radius: 2em;
    /* color: var(--search-box-text); */
    font-size: 16px;
    height: 100%;
    outline: none;
    padding-left: 22px;
    padding-right: 44px;
    width: 100%;
    &:hover {
      box-shadow: 0 1px 3px 0 rgb(0 0 0 / 10%), 0 1px 2px 0 rgb(0 0 0 / 6%);
    }
  }
  .icon-end {
    position: absolute;
    right: 15px;
    top: 0;
    height: 100%;
    width: 24px;
    display: flex;
    align-items: center;
    font-size: 24px;
    svg {
      color: #ff8787;
    }
  }
}
</style>