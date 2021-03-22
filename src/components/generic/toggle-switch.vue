<template>
  <div>

    <label
      :for="id + '_button'"
      :class="{ active: isActive }"
      class="toggle__button flex"
    >
    
    <!-- test Tag here -->
      <span
        class="toggle__label uppercase text-sm mr-3 pt-0.5"
        :class="{ active: isActive == false }"
      >
        test</span
      >

      <input
        type="checkbox"
        :disabled="disabled"
        :id="id + '_button'"
        v-model="checkedValue"
      />

      <span class="toggle__switch"></span>

      <!-- Live Tag here -->
      <span
        class="toggle__label ml-3 text-sm uppercase pt-0.5"
        :class="{ active: isActive == true }"
        >live</span
      >
    </label>

  </div>
</template>

<script>
export default {
  props: {
    disabled: {
      type: Boolean,
      default: false,
    },
    id: {
      type: String,
      default: "primary",
    },
    defaultState: {
      type: Boolean,
      default: true,
    },
  },
  data() {
    return {
      currentState: this.defaultState,
    };
  },
  watch: {
    defaultState: function defaultState() {
      this.currentState = Boolean(this.defaultState);
    },
  },
  computed: {
    isActive() {
      return this.currentState;
    },
    enableText() {
      return this.labelEnableText;
    },
    disabledText() {
      return this.labelDisableText;
    },
    checkedValue: {
      get() {
        return this.currentState;
      },
      set(newValue) {
        this.currentState = newValue;
        this.$emit("change", newValue);
      },
    },
  },
};
</script>

<style scoped>
.toggle__label {
  color: #bdbdbd;
    font-weight: 400;
}
.active {
  color: var(--quad-black);
  font-weight: 500;
}
.toggle__button {
  vertical-align: middle;
  user-select: none;
  cursor: pointer;
}
.toggle__button input[type="checkbox"] {
  opacity: 0;
  position: absolute;
  width: 1px;
  height: 1px;
}
.toggle__button .toggle__switch {
  display: inline-block;
  height: 22px;
  border-radius: 20px;
  width: 44px;
  background: #dadee2 0% 0% no-repeat padding-box;
  position: relative;
  transition: all 0.25s;
}

.toggle__button .toggle__switch::after,
.toggle__button .toggle__switch::before {
  content: "";
  position: absolute;
  display: block;
  height: 20px;
  width: 20px;
  border-radius: 50%;
  left: 0;
  top: 1px;
  transform: translateX(0);
  transition: all 0.25s cubic-bezier(0.5, -0.6, 0.5, 1.6);
}
.toggle__button .toggle__switch::after {
  background: #fff;
  border: 1px solid #dadee2;
}
.toggle__button .toggle__switch::before {
  background: #4d4d4d;
  box-shadow: 0 0 0 3px rgba(0, 0, 0, 0.1);
  opacity: 0;
}
.active .toggle__switch {
  background: #24b57a;
  box-shadow: inset 0 0 1px #adedcb;
}
.active .toggle__switch::after,
.active .toggle__switch::before {
  transform: translateX(40px - 18px);
}
.active .toggle__switch::after {
  border: 1px solid #24b57a;
  left: 23px;
  background: white;
}
</style>