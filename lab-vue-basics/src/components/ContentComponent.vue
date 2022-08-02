<template>
  <div>
    <p>If we multiply {{number1}} by {{number2}}, the result is: {{multiply}}.</p>
    <p v-if="textAppear">If this message appears, the v-if condition should be true</p>
    <button @click="changeTextAppear">Change v-if</button>
  </div>
</template>

<script>
export default {
  name: "ContentComponent",
  data(){
    return{
        number1: 5,
        number2: 3,
        textAppear: true,
    }
  },
  methods: {
    changeTextAppear (){
        this.textAppear = !this.textAppear;
    },
  },
computed: {
    multiply(){
        return this.number1 * this.number2;
    },
},
}
</script>

<style scoped>
div{
    margin: 20px;
}
</style>
