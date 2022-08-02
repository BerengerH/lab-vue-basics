<template>
  <NavComponent />
  <ContentComponent />
  <FooterComponent />
</template>

<script>
import NavComponent from "./components/NavComponent.vue";
import ContentComponent from "./components/ContentComponent.vue";
import FooterComponent from "./components/FooterComponent.vue";

export default {
  name: "App",
  components: {
    NavComponent,
    ContentComponent,
    FooterComponent,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
