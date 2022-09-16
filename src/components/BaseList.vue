<template>
  <div>
    <p v-if="todos.length === 0">
      No todos for now. Please start adding todos!
    </p>
    <ul v-for="(thing, index) in todos" :key="thing">
      <li>
        {{ thing }}
      </li>
      <base-button @click="deleteTodo(index)">Delete</base-button>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {};
  },

  methods: {
    deleteTodo(idx) {
      this.todos.splice(idx, 1);
      // console.log(this.newArr);
    },
  },
  props: ["todos"],
};
</script>
<style scoped>
p {
  color: #005e2dd8;
  font-size: 1.8rem;
}
div {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}
ul {
  display: flex;
  justify-content: space-between;
  /* flex-direction: column; */
}
li {
  list-style: none;
  font-size: 2rem;
  padding: 0.5rem;
  color: #005e2dd8;
  border-bottom: 1px solid #fff;
  /* border-bottom: 1px solid #000; */
}
.delete {
  display: none;
}
</style>
