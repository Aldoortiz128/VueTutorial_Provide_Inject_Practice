<template>
  <section>
    <!--Rendering topicTitle and text based on props-->
    <h2>{{ topicTitle }}</h2>
    <p>{{ text }}</p>
  </section>
</template>

<script>
export default {
  //Passing props to App.vue
  props: ['topicTitle', 'text'],
};
</script>

