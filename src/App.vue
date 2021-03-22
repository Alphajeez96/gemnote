<template>
  <div id="app">
    <div class="flex h-full">
      <div>
      k
        <sideMenu />
      </div>
      <div style="flex-grow: 1">
        <index />
      </div>
    </div>

    <!-- Would serve as template, partials to arry partials. cards to house cards, index.vue to house created cards -->
  </div>
</template>

<script>
import index from "./components/index";
import sideMenu from "./components/partials/sidemenu";

export default {
  name: "App",
  components: {
    index,
    sideMenu,
  },
};
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
