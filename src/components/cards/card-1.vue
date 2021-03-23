<template>
  <div class="flex justify-between flex-wrap">
    <!-- Total orders here -->
    <div class="card-holder pt-5 px-5 pb-6 mb-5  xl:mb-0">
      <p class="text-xs quad-gray font-light">
        Total number of orders this month
      </p>
      <h4 class="sec-gray font-bold text-2xl pt-1">2,736</h4>
      <button
        class="flex items-center mt-1 cursor-auto increase-bg focus:outline-none px-2 text-xs"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="increase-svg"
          width="9"
          height="9"
          viewBox="0 0 9 9"
        >
          <defs>
            <clipPath id="zlnta">
              <path
                d="M2.875.667h5.408v5.408H7.217V2.5L.925 8.792l-.767-.767L6.45 1.733H2.875z"
              />
            </clipPath>
            <clipPath id="zlntb">
              <path d="M-297 828h1366V-196H-297z" />
            </clipPath>
          </defs>
          <g>
            <g>
              <g />
              <g clip-path="url(#zlnta)">
                <g />
                <g clip-path="url(#zlntb)">
                  <path
                    fill="current"
                    d="M-4.842-4.333h18.125v18.125H-4.842z"
                  />
                </g>
              </g>
            </g>
          </g>
        </svg>
        <span class="ml-2">3.5%</span>
      </button>

      <div class="flex justify-end mt-3">
        <button
          type="button"
          class="focus:outline-none seeall-btn flex items-center font-medium px-3.5 py-1.5 font-13"
        >
          <span>View Orders</span>
        </button>
      </div>
    </div>

    <!-- Shipments here -->
    <div class="card-holder pt-5 px-5 pb-6 mb-5 xl:mb-0">
      <p class="text-xs quad-gray font-light">
        Average number of shipments/month
      </p>
      <h4 class="sec-gray font-bold text-2xl pt-1">364</h4>
      <button
        class="flex items-center mt-1 cursor-auto decrease-bg focus:outline-none px-2 text-xs"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="decrease-svg"
          width="9"
          height="9"
          viewBox="0 0 9 9"
        >
          <defs>
            <clipPath id="zlnta">
              <path
                d="M2.875.667h5.408v5.408H7.217V2.5L.925 8.792l-.767-.767L6.45 1.733H2.875z"
              />
            </clipPath>
            <clipPath id="zlntb">
              <path d="M-297 828h1366V-196H-297z" />
            </clipPath>
          </defs>
          <g>
            <g>
              <g />
              <g clip-path="url(#zlnta)">
                <g />
                <g clip-path="url(#zlntb)">
                  <path
                    fill="current"
                    d="M-4.842-4.333h18.125v18.125H-4.842z"
                  />
                </g>
              </g>
            </g>
          </g>
        </svg>
        <span class="ml-2">3.5%</span>
      </button>

      <div class="flex justify-end mt-3">
        <button
          type="button"
          class="focus:outline-none seeall-btn flex items-center font-medium py-1.5 px-3.5 font-13"
        >
          <span>View Shipments</span>
        </button>
      </div>
    </div>

    <!-- Inventory here -->
    <div class="card-holder pt-5 px-5 pb-6">
      <div class="flex justify-between">
        <!-- graph here -->
        <div>
          <Inventory />
        </div>

        <!-- Texts here -->
        <div class="ml-auto text-right">
          <p class="text-xs quad-gray font-light">Current Inventory</p>
          <h4 class="sec-gray font-bold text-2xl pt-1">400</h4>
        </div>
      </div>

      <div class="flex justify-end mt-8">
        <button
          type="button"
          class="focus:outline-none seeall-btn flex items-center font-medium py-1.5 px-3.5 font-13"
        >
          <span>Manage Inventory</span>
        </button>
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
@media (max-width: 575.98px) {
  .card-holder {
    width: 100%;
  }
}

@media (min-width: 576px) and (max-width: 767.98px) {
  .card-holder {
    width: 100%;
  }

}

@media (min-width: 768px) and (max-width: 991.98px) {
  .card-holder {
    width: 100%;
  }
}

@media (min-width: 992px) and (max-width: 1199.98px) {
  .card-holder {
    width: 100%;
  }
}
</style>

