<template>
  <section>
    <!--Forwards to Knowledge-Grid
        This component is acting as a pass-through middleman component. It manages no logic of its own-->
    <!--Topics are passed through from App.vue via props. Select-topic emitter passes the event through to Knowledge Grid-->
    <h2>Select a Topic</h2>
    <!--Emit click listener for 'select-topic' is used here with the $event as a data parameter-->
    <!--Provide+inject removes the need for calling the emit listener here -->
    <knowledge-grid
    ></knowledge-grid>
  </section>
</template>

<script>
export default {
  //Props list
  //Not neccessary with Provide+Inject
  //props: ['topics'],
  //Emit listener list
  //emits: ['select-topic'],
};
</script>