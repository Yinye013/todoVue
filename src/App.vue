<template>
  <div>
    <!-- content to be entered here-->
    <the-header title="To Do App"></the-header>
    <base-card>
      <base-list :todos="thingsToDo"></base-list>
    </base-card>

    <base-input :todo="thingsToDo" :enter="enteredValue"></base-input>
  </div>
</template>
<script>
import TheHeader from "./components/TheHeader.vue";
import BaseCard from "./components/BaseCard.vue";
import BaseList from "./components/BaseList.vue";
import BaseInput from "./components/BaseInput.vue";

export default {
  data() {
    return {
      thingsToDo: [],
    };
  },
  methods: {},
  components: {
    TheHeader,
    BaseCard,
    BaseList,
    BaseInput,
  },
};
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;500;600;700&display=swap");
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html {
  font-size: 62.5%;
  font-family: "Open Sans", sans-serif;
}
</style>
