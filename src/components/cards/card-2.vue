<template>
  <div>
    <div class="card-holder full p-5">
      <p class="text-sm quad-gray font-semibold">
        Trending gifts in your store
      </p>
      <div class="flex justify-between flex-wrap md:flex-nowrap pt-3">
        <!-- Img 1 -->
        <div class="w-full lg:w-1/5 flex items-center justify-center">
          <img src="@/assets/img/products/1.png" alt="" />
        </div>

        <!-- Img 2 -->
        <div class="w-full lg:w-1/5 flex items-center justify-center">
          <img src="@/assets/img/products/2.png" alt="" />
        </div>

        <!-- Img 3 -->
        <div class="w-full lg:w-1/5 flex items-center justify-center">
          <img src="@/assets/img/products/3.png" alt="" />
        </div>

        <!-- Img 4 -->
        <div class="w-full lg:w-1/5 flex items-center justify-center">
          <img src="@/assets/img/products/4.png" alt="" />
        </div>

        <!--Send Gift button here -->
        <div
          class="mt-8 flex items-start w-full justify-center lg:w-1/5 lg:justify-end"
        >
          <button
            type="button"
            class="focus:outline-none seeall-btn flex items-center w-full justify-center font-medium py-2 md:px-1 px-5 font-13"
          >
            <span>Send a gift</span>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>
