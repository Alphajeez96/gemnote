<template>
  <nav class="relative hidden">
    <!-- Notification drop down -->
    <notificationDropdown v-if="isNotificationOpen" @close="closeNotify" />
    <profileTab v-if="isProfileTabOpen" />

    <div class="flex px-6">
      <div class="self-center">
        <h4 class="font-bold text-2xl route">{{ route }}</h4>
      </div>

      <div class="ml-auto flex self-center items-center relative">
        <!-- search bar here -->
        <div class="relative mx-6">
          <img
            src="@/assets/img/vectors/search-icon.svg"
            class="absolute search"
            alt="search"
          />
          <input
            type="text"
            class="focus:outline-none search-control px-10"
            placeholder="Search gifts, customer etc"
          />
        </div>

        <div class="border-left"></div>

        <div class="border-left"></div>

        <!--notification menu here  -->
        <div class="mx-6 hidden">
          <img
            src="@/assets/img/vectors/ic-notification.svg"
            alt="User"
            class="cursor-pointer"
            @click="openNotify"
          />
        </div>

        <div class="border-left mr-6"></div>

        <!--profile menu here  -->
        <div>
          <img
            src="@/assets/img/vectors/ic-profile-placeholder.svg"
            alt="User"
            class="cursor-pointer"
            @click="openprofileTab"
          />
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
import notificationDropdown from "@/components/generic/notification-dropdown";
import profileTab from "@/components/generic/profile-dropdown";
export default {
  data: () => ({
    route: "Dashboard",
    isNotificationOpen: false,
    isProfileTabOpen: false,
  }),

  components: {
    notificationDropdown,
    profileTab,
  },

  methods: {
    closeNotify() {
      this.isNotificationOpen = false;
    },

    openNotify() {
      this.isNotificationOpen = !this.isNotificationOpen;
      if (this.isProfileTabOpen == true) {
        this.isProfileTabOpen = false;
      }
    },

    openprofileTab() {
      this.isProfileTabOpen = !this.isProfileTabOpen;
      if (this.isNotificationOpen == true) {
        this.isNotificationOpen = false;
      }
    },
  },
};
</script>

<style scoped>
nav {
  background: #ffffff 0% 0% no-repeat padding-box;
  border: 1px solid #dadee2;
  height: 72.5px;
}

.border-left {
  border-left: 1px solid #dadee2;
  height: 70px;
}
.search-control {
  background: #f5f5f5 0% 0% no-repeat padding-box;
  box-shadow: 0px 2px 2px #3f3f4419;
  border-radius: 4px;
  height: 40px;
  width: 22.813rem;
}
.search {
  top: 13px;
  left: 13px;
}
.search-control::placeholder {
  color: #646a86;
  font-size: 0.875rem;
  opacity: 0.5;
}

@media (max-width: 575.98px) {
.search-control{
}
}

@media (min-width: 576px) and (max-width: 767.98px) {}
</style>