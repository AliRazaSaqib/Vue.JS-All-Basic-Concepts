<template>
  <div class="content-body">
    <div class="content">
      <table border="2px" color="white" class="tableData">
        <tr>
          <td>ID</td>
          <td>Name</td>
        </tr>
        <tr
          v-for="data in apiInfo"
          :key="data.id"
          @click="handleRowClick(data.id)"
        >
          <td>{{ data?.id }}</td>
          <td>{{ data?.title }}</td>
        </tr>
      </table>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  //import component
  name: "DataFile",

  // json object
  data() {
    return {
      apiInfo: null,
    };
  },

  mounted() {
    const apiResp = axios
      .get("https://jsonplaceholder.typicode.com/todos")
      .then((response) => (this.apiInfo = response?.data));
  },

  methods: {
    handleRowClick(key) {
      console.log(key);
    },
  },

  // return {
  //   users: [
  //     {
  //       id: 1,
  //       name: "Ali",
  //     },
  //     {
  //       id: 2,
  //       name: "Umer",
  //     },
  //     {
  //       id: 3,
  //       name: "Afaq",
  //     },
  //     {
  //       id: 4,
  //       name: "Asif",
  //     },
  //   ],
  // };
};
</script>

<style>
.content-body {
  background-color: chocolate;
  color: white;
}
.content {
  padding: 24px;
}
.tableData {
  width: 100%;
  max-height: 200px;
  height: 100%;
  overflow-y: auto;
}
</style>
