<template>
  <div id="app">
    <div class="flex">
      <div>
        <sideMenu />
      </div>
      <div style="flex-grow: 1">
        <topNav />
        <index />
      </div>
    </div>
  </div>
</template>

<script>
import index from "./components/index";
import sideMenu from "./components/partials/sidemenu-2";
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
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-family: "Hero New ";
  background: #f4f6f8;
}
.primary-blue {
  color: #2843b4;
}
.quad-gray {
  color: #7c8191;
}
.primary-gray {
  color: #646a86;
}

.sec-gray {
  color: #74787c;
}
.font-13 {
  font-size: 0.813rem;
}
.sec-blavk {
  color: #1b1c1d;
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

.graph {
  border-radius: 50%;
  height: 50px;
  width: 50px;
  background: #74787c;
}
</style>
