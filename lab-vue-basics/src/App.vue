<template>
  <NavComponent/>
  <ContentComponent @test="calculate" :items="items"/>
  <p>Final result in parent is: {{number}}</p>
  <FooterComponent/>
  <ContentComponent2 
  v-for="item in items"
  :title="item.title"
  :description="item.description"
  :content="item.content"
  />
</template>

<script>
import NavComponent from "./components/NavComponent.vue";
import ContentComponent from "./components/ContentComponent.vue";
import FooterComponent from "./components/FooterComponent.vue";
import ContentComponent2 from "./components/ContentComponent2.vue";


export default {
  name: "App",
  components: {
    NavComponent,
    ContentComponent,
    FooterComponent,
    ContentComponent2,
},
    data() {
    return {
      items: [
        { title: "Title 1", description: "Description 1", content: "Content 1" },
        { title: "Title 2", description: "Description 2", content: "Content 2" },
        { title: "Title 3", description: "Description 3", content: "Content 3" },
      ],
      number: 0,
    };
  },
  methods: {
    calculate(data){
      console.log("button calculate was clicked");
      this.number++;
    },
  }
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
