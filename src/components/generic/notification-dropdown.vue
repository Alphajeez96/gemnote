<template>
  <div>
    <div class="holder absolute p-4">
      <div class="flex">
        <p class="pt-2 sec-black font-light font-13">Platform update</p>

        <div class="ml-auto self-center pt-2">
          <button @click="close" type="button" class="focus:outline-none">
            <img src="@/assets/img/vectors/ic-close.svg" alt="close" />
          </button>
        </div>
      </div>

      <p class="pt-3 font-13 font-light primary-gray">
        Now, your customers can do this and that, add this and be happy, blast
        black . . .
      </p>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    close() {
      this.$emit("close");
    },
  },
};
</script>

<style scoped>
.holder {
  background: #ffffff 0% 0% no-repeat padding-box;
  box-shadow: 0px 3px 6px #00000029;
  border: 1px solid #e7eaed;
  border-radius: 3px;
  width: 271px;
  z-index: 99999999;
  right: 20px;
  top: 77px;
}
</style>