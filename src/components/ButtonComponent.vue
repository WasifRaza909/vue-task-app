<template>
  <button
    :style="{
      background: color,
    }"
    @click="onClick()"
    class="btn"
  >
    {{ text }}
  </button>
</template>

<script>
export default {
  name: "ButtonComponent",
  props: {
    text: String,
    color: String,
  },
  methods: {
    onClick() {
      this.$emit("btn-click");
    },
  },
};
</script>
