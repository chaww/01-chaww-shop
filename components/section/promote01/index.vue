<template>
  <div class="section-bg">
    <slot name="bg"></slot>
    <div class="wrapper">
      <div class="container">
        <div class="image">
          <img class="circle" src="~/assets/images/product_01.jpg" />
        </div>
        <div class="content">
          <div>
            <h2>Kofe Point Arabica 100%</h2>
            <h3>(Arabica)</h3>
            <div class="description">
              <p>Sale 40%</p>
            </div>
            <h1 class="price">
              480 ฿ <span class="price-over"> 800 ฿</span>
            </h1>
            <div class="button-wrapper"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style scoped lang="scss">
/* .section-bg {
  background-color: var(--color_bg_page_soft);
} */
.wrapper {
  padding-top: 100px;
}
.container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: center;
}
.image {
  width: 50vw;
  display: flex;
  justify-content: flex-end;
  margin-right: 50px;
  .circle {
    height: 400px;
    width: 400px;
    border: 1px var(--color_text_soft) solid;
    border-radius: 400px;
  }
}
.content {
  width: 50vw;
  display: flex;
  justify-content: flex-start;
  align-items: center;
  margin-left: 50px;
  p {
    color: var(--color_text_soft);
  }
  .description {
    margin-top: 1em;
  }
  .price {
    margin-top: 1em;
    display: flex;
    align-items: center;
    .price-over{
      color: var(--color_text_soft);
      margin-left: 15px;
      font-size: 0.5em;
      font-weight: 500;
      text-decoration: line-through;
    }
  }
}
</style>