<template>
  <button>
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "my-button",
};
</script>

<style scoped>
button {
  padding: 10px 15px;
  border: 1px solid teal;
  background: none;
  color: teal;
  cursor: pointer;
}
</style>
