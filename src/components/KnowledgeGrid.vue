<template>
  <ul>
    <!--Only manages topics data
    --Topics are passed through from Knowledge-Grid.vue via props. However, as opposed to KnowledgeBase, it is doing something with this data.
    Select-topic emitter passes the event through to App.vue-->
    <!--Forwards to Knowledge-Element-->
    <!--Emit click listener for 'select-topic' is used here with the $event as a data parameter-->
    <!--Provide+inject eliminates the need for calling the emit listener here-->
    <knowledge-element
      v-for="topic in topics"
      :key="topic.id"
      :id="topic.id"
      :topic-name="topic.title"
      :description="topic.description"
    ></knowledge-element>
  </ul>
</template>

<script>
export default {
  //Inject is used here to pass through our data from provide from App.vue
  inject: ['topics'],
  //Provide+Inject eliminates the need for using the emits option here
 // emits: ['select-topic'],
};
</script>