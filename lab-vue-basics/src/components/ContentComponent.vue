<template>
  <div class="" :class="[background ? '' : 'backgroundBlue']">
    <p>
      If we multiply {{ number1 }} by {{ number2 }}, the result is:
      {{ multiply }}.
    </p>
    <p v-if="textAppear">
      If this message appears, the v-if condition should be true
    </p>
    <button @click="changeTextAppear">Change v-if</button>
    <button @click="changeBackground">Change background</button>
  </div>
</template>

<script>
export default {
  name: "ContentComponent",
  data() {
    return {
      number1: 5,
      number2: 3,
      textAppear: true,
      background: true,
      items: [
        { title: "Title One", description: "", content: "" },
        { title: "Title One", description: "", content: "" },
        { title: "Title One", description: "", content: "" },
      ],
    };
  },
  methods: {
    changeTextAppear() {
      this.textAppear = !this.textAppear;
    },
    changeBackground() {
      this.background = !this.background;
    },
  },
  computed: {
    multiply() {
      return this.number1 * this.number2;
    },
  },
};
</script>

<style scoped>
div {
  margin: 20px;
  color: red;
}

.backgroundBlue {
  background-color: #72ffff;
}
</style>
