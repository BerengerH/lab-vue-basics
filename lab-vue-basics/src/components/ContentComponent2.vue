<template>
        <div>
            <p>{{title}}</p>
            <p>{{description}}</p>
            <p>{{content}}</p>
        </div>
</template>

<script>
export default {
  name: "ContentComponent2",
  props: {
     'title': String,
     'description': String,
     'content': String,
  },
};
</script>

<style scoped>
</style>
