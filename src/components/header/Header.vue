<template>
  <div class="header">
    <div class="hd">
      I am header
      <p>{{ data }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: {
    data: String,
  },
};
</script>

<style scoped>
.header {
  background-color: bisque;
  width: 100%;
}

.hd {
  padding: 12px 24px;
}
</style>
