<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
import store from '@/store';

export default {
  name: 'app',
  store,
  created() {
    this.$store.dispatch('authenticate');
  },
};
</script>

<style>
  @font-face {
    font-family: "Skolar";
    src: url("https://jktauber.com/site_media/static/fonts/SkolarPEWeb-Regular.woff") format("woff");
    font-style: normal;
    font-weight: normal;
    text-rendering: optimizeLegibility;
  }
  @font-face {
    font-family: "Skolar";
    src: url("https://jktauber.com/site_media/static/fonts/SkolarPEWeb-Italic.woff") format("woff");
    font-style: italic;
    font-weight: normal;
    text-rendering: optimizeLegibility;
  }
  @font-face {
    font-family: "Skolar";
    src: url("https://jktauber.com/site_media/static/fonts/SkolarPEWeb-Bold.woff") format("woff");
    font-style: normal;
    font-weight: bold;
    text-rendering: optimizeLegibility;
  }

  body {
    margin: 0;
    -webkit-font-smoothing: antialiased;
    font-feature-settings: "ccmp";
  }
</style>
