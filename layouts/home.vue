<template>
  <div>
    <!-- <MainHeader :navheight="'150px'"/> -->
    <MainHeader class="mainheader"/>
    <Nuxt class="nuxt"/>
    <!-- <MainFooter /> -->
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import MainHeader from '@/components/layouts/MainHeader/MainHeader.vue'
// import MainFooter from '@/components/layouts/MainFooter/MainFooter.vue'

export default Vue.extend({
  data() {
    return {}
  },
  components: {
    MainHeader,
    // MainFooter,
  },
})
</script>
<style>
.mainheader{
  position: fixed;
}
.nuxt{
  padding-top: 129px;
}
</style>