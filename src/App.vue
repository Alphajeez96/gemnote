<template>
  <div id="app">
    <div class="flex">
      <div class="hidden xl:block ">
        <sideMenu />
      </div>
      <div class="flex-grow">
        <topNav />
        <index />
      </div>
    </div>
  </div>
</template>

<script>
import index from "./components/index";
import sideMenu from "./components/partials/sidemenu";
import topNav from "./components/partials/topnav";

export default {
  name: "App",
  components: {
    index,
    sideMenu,
    topNav,
  },
};
</script>

<style>
:root {
  --primary-gray: #646a86;
  --sec-gray: #74787c;
  --quad-gray: #7c8191;
  --sec-black: #1b1c1d;
}
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-family: "Hero New ";

}

html, body{
  background: #f4f6f8;
}

.primary-gray {
  color: var(--primary-gray);
}

.sec-gray {
  color: var(--sec-gray);
}

.quad-gray {
  color: var(--quad-gray);
}
.sec-black {
  color: var(--sec-black);
}

.font-13 {
  font-size: 0.813rem;
}

.route {
  color: #464646;
}

.card-holder {
  background: #ffffff 0% 0% no-repeat padding-box;
  border: 1px solid #e7eaed;
  border-radius: 3px 3px 0px 0px;
  width: 346px;
}
.card-holder.full {
  width: 100%;
}
.increase-bg {
  background: #24b47a26 0% 0% no-repeat padding-box;
  border-radius: 3px;
  height: 18px;
  color: #24b47a;
}
.increase-svg {
  fill: #24b47a;
}
.decrease-bg {
  background: #f1d6d6 0% 0% no-repeat padding-box;
  border-radius: 3px;
  height: 18px;
  color: #b52424;
}

.decrease-svg {
  fill: #b52424;
}
.seeall-btn {
  background: #ffffff 0% 0% no-repeat padding-box;
  box-shadow: 0px 2px 2px rgb(63 63 68 / 30%);
  border: 1px solid #e7eaed;
  border-radius: 3px;
  font-size: 0.813rem;
  color: #74787c;
}

@media (max-width: 575.98px) {

canvas#bar-chart{
width: 343px !important;
}
}

@media (min-width: 576px) and (max-width: 767.98px) {}


</style>
