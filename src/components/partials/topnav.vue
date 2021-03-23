<template>
  <nav class="relative">
    <!-- Notification drop down -->
    <notificationDropdown v-if="isNotificationOpen" @close="closeNotify" />
    <profileTab v-if="isProfileTabOpen" />

    <div class="flex items-center py-2.5 lg:py-0 lg:px-6 px-3">
      <!-- Hamburger here -->
      <div class="self-center lg:hidden mr-3">
        <img src="../../assets/img/vectors/ic-nav.svg" @click="test" alt="Hamburger" />
      </div>

      <!-- Route holder here -->
      <div class="self-center">
        <h4 class="font-bold text-xl lg:text-2xl route">{{ route }}</h4>
      </div>

      <div class="ml-auto flex self-center items-center relative">
        <!-- search bar here -->
        <div class="relative mx-6 hidden">
          <img
            src="@/assets/img/vectors/search-icon.svg"
            class="absolute search"
            alt="search"
          />
          <input
            type="text"
            class="focus:outline-none search-control px-8 lg:px-10"
            placeholder="Search gifts, customer etc"
          />
        </div>

        <div class="relative mx-2 lg:hidden">
          <img
            src="@/assets/img/vectors/search-icon.svg"
            class="absolute search"
            alt="search"
          />
          <input
            type="text"
            class="focus:outline-none text-xs search-control px-7"
            placeholder="Search "
          />
        </div>

        <div class="border-left hidden lg:block"></div>

        <div class="border-left hidden lg:block"></div>

        <!--notification menu here  -->
        <div class="mx-6 hidden">
          <img
            src="@/assets/img/vectors/ic-notification.svg"
            alt="User"
            height="35"
            width="35"
            class="cursor-pointer"
            @click="openNotify"
          />
        </div>

        <div class="border-left mr-6 hidden lg:block"></div>

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

    test(){
      console.log("i was clicked")
      this.$emit("clicked")
    }
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
  nav {
    height: auto;
  }
  .search-control {
    width: 95px;
    height: 32px;
  }
  .search-control::placeholder {
    font-size: 0.75rem;
  }
  .search {
    top: 9px;
    left: 9px;
  }
}

@media (min-width: 576px) and (max-width: 767.98px) {
}
</style>