<!--Render Element for each individual Topic-->
<template>
  <li>
    <h3>{{ topicName }}</h3>
    <p>{{ description }}</p>
    <!--Provide+Inject removes the need for the 'select-topic' emit listener here-->
    <!--Here we can bind the selectTopic element that was passed down as props.
		We can also pass down the id prop so we know which topic is selected.
		-->
    <button @click="selectTopic(id)">Learn More</button>
  </li>
</template>

<script>
export default {
  //selectTopic() is passed down via Inject
	inject:['selectTopic'],
  props: ['id', 'topicName', 'description'],
  //emits: ['select-topic'],
};
</script>