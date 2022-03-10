<template>
  <button :class="[variant, size, color]">
    <span class="material-icons starticon" v-if="$props.startIcon">
      {{ startIcon }} </span
    ><slot>Default</slot>
    <span class="material-icons endicon" v-if="$props.endIcon">
      {{ endIcon }}
    </span>
  </button>
</template>
<script>
export default {
  name: "ButtonComponent",
  props: {
    size: {
      type: String,
      default: "md",
      validator(value) {
        return ["sm", "md", "lg"].includes(value);
      },
    },
    variant: {
      type: String,
      validator(value) {
        return ["outline", "text"].includes(value);
      },
    },
    color: {
      type: String,
      validator(value) {
        return ["primary", "secondary", "default", "danger"].includes(value);
      },
    },
    startIcon: {
      type: String,
    },
    endIcon: {
      type: String,
    },
  },
  data() {
    return {};
  },
};
</script>
<style scoped>
/**default stage */
button {
  height: max-content;
  width: max-content;
  padding: 8px 16px;
  background-color: #e0e0e0;
  font-family: "Noto Sans", sans-serif;
  font-weight: 500;
  font-size: 14px;
  line-height: 20.27px;
  border: none;
  border-radius: 6px;
  color: #3f3f3f;
  box-shadow: 0px 2px 3px rgba(51, 51, 51, 0.2);
}
button:hover,
button:focus {
  background-color: #aeaeae;
}
/**variant styles */
.outline {
  border: 1px solid #3d5afe;
}
.text,
.outline {
  color: #3d5afe;
  background-color: white;
  box-shadow: none;
}
.text:hover,
.text:focus,
.outline:hover,
.outline:focus {
  background-color: rgba(41, 98, 255, 0.1);
}
/**differnt sizes */
.sm {
  padding: 6px 12px;
}
.lg {
  padding: 11px 22px;
}
/**colors primary,secondary,danger,default */
.primary {
  background-color: #2962ff;
  box-shadow: 0px 2px 3px rgba(41, 98, 255, 0.2);
}
.secondary {
  background-color: #455a64;
  box-shadow: 0px 2px 3px rgba(69, 90, 100, 0.2);
}
.danger {
  background-color: #d32f2f;

  box-shadow: 0px 2px 3px rgba(211, 47, 47, 0.2);
}
.primary,
.secondary,
.danger {
  color: #ffffff;
}
.primary:hover,
.primary:focus {
  background-color: #0039cb;
}
.secondary:hover,
.secondary:focus {
  background-color: #1c313a;
}
.danger:hover,
.danger:focus {
  background-color: #9a0007;
}
/**styling for icons */
.material-icons {
  font-size: 14px;
  line-height: 20.27px;
}
.starticon {
  padding: 0px 10px 0px 0px;
}
.endicon {
  padding: 0px 0px 0px 10px;
}

/**disabled and disabledShadow */
button[disabled] {
  color: #9e9e9e;
}
button[disabledShadow] {
  box-shadow: none;
}
</style>
