<template>
  <div class="" :class="[background ? '' : 'backgroundBlue']">
    <input type="number" v-model="number1">
    <input type="number" v-model="number2">
    <p>
      If we multiply {{ number1 }} by {{ number2 }}, the result is:
      {{ multiply }}.
    </p>
    <p v-if="textAppear">
      If this message appears, the v-if condition should be true
    </p>
    <button @click="changeTextAppear">Change v-if</button>
    <button @click="changeBackground">Change background</button>
    <div class="flex">
        <div v-for="item in items">
            <p>{{ item.title }}</p>
            <p>{{ item.description }}</p>
            <p>{{ item.content }}</p>
        </div>
    </div>
    <li >
</li>

  </div>
</template>

<script>
export default {
  name: "ContentComponent",
  data() {
    return {
      number1: 0,
      number2: 0,
      textAppear: true,
      background: true,
      items: [
        { title: "Title 1", description: "Description 1", content: "Content 1" },
        { title: "Title 2", description: "Description 2", content: "Content 2" },
        { title: "Title 3", description: "Description 3", content: "Content 3" },
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
}

.backgroundBlue {
  background-color: #72ffff;
}

.flex{
    display: flex;
    justify-content: space-between;
    gap: 10px;
}
</style>
