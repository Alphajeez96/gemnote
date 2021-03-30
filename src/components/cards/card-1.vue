<template>
  <div class="flex flex-wrap xl:flex-nowrap">
    <!-- card 1 here -->
    <div class="card-holder p-5 w-full">
      <div class="flex">
        <!-- Total number here -->
        <div class="w-1/2">
          <h5 class="text-base primary-black font-medium">
            Total number of <br />
            orders this month
          </h5>
          <h4 class="text-3xl lg:text-4xl sec-black font-semibold pt-5">
            2,736
          </h4>
        </div>

        <!-- divider here -->
        <div class="divider pr-4 md:pr-8 xl:pr-8"></div>

        <!-- Average number here -->
        <div class="w-1/2">
          <h5 class="text-base primary-black font-medium">
            Average number of shipments/month
          </h5>

          <div class="flex items-center">
            <h4 class="text-3xl lg:text-4xl sec-black font-semibold pt-5">
              364
            </h4>

            <div class="ml-auto self-end">
              <button
                type="button"
                class="focus:outline-none bg-transparent font-13 py-2 px-2 lg:px-3.5 font-medium primary-btn"
              >
                View Orders
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- card 2 here -->
    <div class="card-holder p-5 w-full xl:ml-6 mt-7 xl:mt-0">
      <div class="flex justify-between">
        <!-- chart here -->

        <div>
          <inventory />
        </div>

        <div class="w-3/5">
          <!-- current Invemtory -->
          <h5 class="text-base primary-black font-medium">Current Inventory</h5>

          <div class="flex items-center">
            <h4 class="text-3xl lg:text-4xl sec-black font-semibold pt-5">
              400
            </h4>

            <div class="ml-auto self-end">
              <button
                type="button"
                class="focus:outline-none bg-transparent font-13 py-2.5 px-2 font-medium primary-btn"
              >
                Manage Inventory
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Inventory from "../charts/inventory";
export default {
  components: {
    Inventory,
  },
};
</script>

<style scoped>
.divider {
  border-left: 2px solid #e5e5e5;
}

</style>

