<template>
  <div>
    <div class="holder absolute px-3">
      <ul>
        <li
          class="font-13 primary-gray py-3 border-b font-light tab-link"
          v-for="(link, index) in links"
          :key="index"
        >
          <router-link to>{{ link }}</router-link>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    links: [
      "Settings",
      "Notifications",
      "Documentation",
      "Get Started",
      "Logout",
    ],
  }),
};
</script>

<style scoped>
.holder {
  background: #ffffff 0% 0% no-repeat padding-box;
  box-shadow: 0px 3px 6px #00000029;
  border: 1px solid #e7eaed;
  border-radius: 3px;
  width: 142px;
  z-index: 99999999;
  right: 5px;
  top: 77px;
}

.tab-link:hover {
  color: #2843b4;
  font-weight: 400;
}
.border-b {
  border-bottom: 1px solid #e7eaed;
}

@media (max-width: 575.98px) {
  .holder {
    top: 55px;
  }
}

@media (min-width: 576px) and (max-width: 767.98px) {
  main {
    top: 55px;
  }
}
</style>