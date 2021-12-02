<template>
  <nav class="navbar">
    <div class="navbar-top">
      <Left />
      <Right />
    </div>
    <div class="navbar-sub">
      <Logo class="logo-component" />
      <div class="search">
        <FormInputText />
      </div>
      <div class="cart">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="24px"
          height="24px"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="feather feather-shopping-cart"
        >
          <circle cx="9" cy="21" r="1"></circle>
          <circle cx="20" cy="21" r="1"></circle>
          <path
            d="M1 1h4l2.68 13.39a2 2 0 0 0 2 1.61h9.72a2 2 0 0 0 2-1.61L23 6H6"
          ></path>
        </svg>
      </div>
    </div>
  </nav>
</template>

<script lang="ts">
import Vue from 'vue'
import Left from './Left.vue'
import Right from './Right.vue'
import Logo from './Logo.vue'

export default Vue.extend({
  // props: {
  //   navheight: String,
  // },
  data() {
    return {}
  },
  components: {
    Left,
    Right,
    Logo,
  },
})
</script>

<style scoped lang="scss">
.navbar {
  width: 100%;
  background-color: #f9f9f9;
  z-index: 1000; // navbar 1000-1100
}
.navbar-top,
.navbar-sub {
  width: 100%;
  height: 35px;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 15px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.navbar-sub {
  height: fit-content;
  padding: 10px 15px;
  height: 100%;
  .logo-component:hover {
    cursor: pointer;
  }
  .search {
    width: 100%;
    display: flex;
    align-items: center;
    margin-right: 15px;
    padding: 15px 0;
    height: 100%;
    width: 100%;
  }
  .cart {
    height: 100%;
    width: 44px;
    display: flex;
    justify-content: center;
    align-items: center;
    &:hover {
      cursor: pointer;
    }
  }
  .feather.feather-shopping-cart {
    color: #aaaaaa;
  }
}
</style>