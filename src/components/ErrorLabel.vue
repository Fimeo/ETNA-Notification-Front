<template>
  <div class="error-wrapper">
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  name: "ErrorLabel",
  props: {
    message: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
.error-wrapper {
  margin: 15px 0;
  padding: 15px 20px;
  display: block;
  background: rgba(156, 0, 36, 0.25);
}
</style>
