<template>
  <div class="bg-container">
    <h2>Data binding</h2>

    <p style="white-space: pre-line">{{ name }}</p>
    <textarea type="text" v-model="name" />
    <!-- <input type="text" v-model="name" /> -->
  </div>
</template>

<script>
export default {
  name: "DataBinding",

  // add properties
  data() {
    return {
      name: "ali",
    };
  },
};
</script>

<style>
.bg-container {
  background-color: bisque;
  color: black;
  border-radius: 12px;
  padding: 12px;
  margin-top: 24px;
}
</style>
