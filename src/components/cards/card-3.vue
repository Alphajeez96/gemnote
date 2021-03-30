<template>
  <div>
    <div class="card-holder full p-5">
      <div class="flex pt-3 pb-5">
        <p class="text-sm primary-black font-semibold">
          Total gifts sent this year
        </p>

        <div class="ml-auto self-center">
          <button
            type="button"
            class="focus:outline-none bg-transparent font-13 py-2.5 px-7 font-medium primary-btn"
          >
            Download report
          </button>
        </div>
      </div>

      <!-- chart here -->
      <div>
        <giftChart />
      </div>
    </div>
  </div>
</template>

<script>
import giftChart from "../charts/total-gifts";
export default {
  components: {
    giftChart,
  },
};
</script>
