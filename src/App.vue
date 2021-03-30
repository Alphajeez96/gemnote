<template>
  <div id="app">


    <!-- screen Layout here -->
    <div class="flex">
      <div class=" md:block xl:block">
        <sideMenu />
      </div>

      <div class="flex-grow">
        <index />
      </div>
    </div>
  </div>
</template>

<script>
import index from "./components/index";
import sideMenu from "./components/partials/sidemenu";

export default {
  name: "App",

  data: () => ({
    IsVisible: false,
  }),

  components: {
    index,
    sideMenu,
  },

};
</script>

<style>
:root {
  --primary-black: #25282a;
  --sec-black: #24292c;
}
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-family: "Hero New ";
}

html,
body {
  background: #ffffff;
}

.primary-black {
  color: var(--primary-black);
}

.sec-black {
  color: var(--sec-black);
}
.font-13 {
  font-size: 0.813rem;
}
.card-holder {
  background: inherit;
  border: 2px solid #e3e3e3;
  border-radius: 3px 3px 0px 0px;
}

.primary-btn {
  border: 2px #919495;
  color: #323639;
  border-style: solid solid double solid;
}

.primary-btn:hover {
  background: #919495;
  border-radius: 3px;
  color: #fff;
}

@media (max-width: 575.98px) {
  canvas#bar-chart {
    width: 343px !important;
  }
}

@media (min-width: 576px) and (max-width: 767.98px) {
  canvas#bar-chart {
    width: 343px !important;
  }
}
</style>
