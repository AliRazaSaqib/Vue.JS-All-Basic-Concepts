<template>
  <div class="bg-container">
    <h3>Props Concept</h3>
    <table border="2px" color="white" class="tableData">
      <tr>
        <td>ID</td>
        <td>Name</td>
        <td>Work</td>
      </tr>
      <tr v-for="user in userInfo" :key="user.id">
        <td>{{ user?.id }}</td>
        <td>{{ user?.name }}</td>
        <td>{{ user?.work }}</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: "PropsConcept",

  props: ["userInfo"],
};
</script>

<style scoped>
.bg-container {
  background-color: bisque;
  color: black;
  border-radius: 12px;
  padding: 12px;
  margin-top: 24px;
}
</style>
