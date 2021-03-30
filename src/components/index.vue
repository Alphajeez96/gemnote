<template>
  <div class="py-10 mx-6 lg:mx-24">
    <h4 class="font-bold pb-2 text-xl lg:text-2xl route">
      Welcome to Gemnote, Ashley!
    </h4>

    <!-- cars 1 here -->
    <div class="mt-7">
      <card1 />
    </div>

    <!-- cars 2 here -->
    <div class="mt-7">
      <card2 />
    </div>

    <!-- cars 3 here -->
    <div class="mt-7">
      <card3 />
    </div>
  </div>
</template>

<script>
import card1 from "./cards/card-1";
import card2 from "./cards/card-2";
import card3 from "./cards/card-3";
export default {
  components: {
    card1,
    card2,
    card3,
  },
};
</script>
