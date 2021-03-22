<template>
  <main class="h-full">
    <transition name="fade">
      <nav id="sidebar" class="w-60">
        <div class="flex p-6">
          <!--Company Name here -->
          <div><p class="font company-name text-base">Akaraka Limited</p></div>
          <div class="ml-auto">
            <button type="button" class="focus:outline-none">
              <img src="" alt="Bar" />
            </button>
          </div>
        </div>
        <hr />

        <!--Routes here -->
        <div class="px-6 py-5">
          <ul class="flex list-decimal flex-col">
            <li v-for="(route, index) in routes" :key="index">
              <router-link :to="route" class="flex mb-2.5">
                <span class="pt-1 ml-2.5">{{ route }}</span>
              </router-link>
            </li>
          </ul>
        </div>
      </nav>
    </transition>
  </main>
</template>

<script>
export default {
  data() {
    return {
      routes: ["Dashboard"],
    };
  },

  props: {
    step: {
      type: Number,
    },
  },
};
</script>

<style scoped>
#sidebar {
  height: 100%;
}
main {
  background: #222840 0% 0% no-repeat padding-box;
}

.company-name {
  color: #e7eaf3;
  font-family: "Circular Std";
}

#sidebar ul li {
  color: #e3e4e7;
  font-weight: 300;
  font-size: 0.875rem;
  list-style: none;
}

hr {
  border-top: 1px solid #babfc6;
}
.nav-link-header {
  color: #d0f0fd;
  font-family: "Circular Std";
  letter-spacing: 0px;
}

.square {
  fill: #bbc4e6;
}

.square.active {
  fill: var(--primary-blue);
}

.sidebar-link.active {
  /* color: var(--primary-blue); */
  color: #d0f0fd;
}
</style>