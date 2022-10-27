<template>
  <Header data="props from header" />
  <Content data="props from body" />
  <Footer data="props from footer" />
</template>

<script>
import Header from "./components/header/Header.vue";
import Footer from "./components/footer/Footer.vue";
import Content from "./components/body/Content.vue";

export default {
  name: "App",
  components: {
    Header,
    Content,
    Footer,
  },
};
</script>
,

<style>
body {
  padding: 0;
  margin: 0;
}
</style>
