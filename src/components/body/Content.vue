<template>
  <div class="content-body">
    <div class="content">
      Overall content
      <p>{{ data }}</p>

      <button @mouseover="hello('hello')">Click me</button>

      <div class="content-toggle">
        <p v-if="show">Show Data</p>
        <p v-else>Nothing is availble to show</p>
        <button @click="displayContent()">Toggle</button>
      </div>

      <!-- data binding -->
      <DataBinding />

      <!-- PropsConcept -->
      <PropsConcept v-bind:userInfo="userInfo" />

      <!-- Use dataFile here -->
      <DataFile />
    </div>
  </div>
</template>

<script>
import DataFile from "./DataFile.vue";
import DataBinding from "../body/DataBinding.vue";
import PropsConcept from "../body/PropsConcept.vue";

export default {
  //import component
  name: "Content",

  //props
  props: {
    data: String,
  },
  // data functions
  data() {
    return {
      show: true,

      userInfo: [
        { id: 1, name: "ali", work: "Frontend developer" },
        { id: 2, name: "afaq", work: "BI developer" },
      ],
    };
  },
  // methods / functions
  methods: {
    hello(data) {
      alert(data);
      //   console.log("I am clicked");
    },

    displayContent() {
      this.show = !this.show;
    },
  },

  components: {
    DataFile,
    DataBinding,
    PropsConcept,
  },
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

.content-toggle {
  background-color: whitesmoke;
  padding: 12px;
  color: black;
  margin-top: 24px;
  border-radius: 12px;
}
</style>
