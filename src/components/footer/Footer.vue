<template>
  <div class="footer-parent">
    <div class="footer">
      <div class="ft">
        I am Footer
        <p>{{ data }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
  props: {
    data: String,
  },
};
</script>

<style scoped>
.footer-parent {
  position: relative;
}

.footer {
  background-color: aquamarine;
  width: 100%;

  position: absolute;
}
.ft {
  padding: 12px 24px;
}
</style>
