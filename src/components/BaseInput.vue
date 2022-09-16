<template>
  <div>
    <form action="/" @submit.prevent="addList">
      <input
        type="text"
        placeholder="Add to-do here..."
        v-model="enteredValue"
      />
      <base-button>Add To-do List</base-button>
    </form>
  </div>
</template>
<script>
export default {
  props: ["todo"],

  data() {
    return {
      enteredValue: " ",
    };
  },
  methods: {
    addList() {
      if (this.enteredValue === " ") {
        alert("Type something!");
      } else if (this.enteredValue === 0) {
        alert("Type something!");
      } else {
        this.todo.push(this.enteredValue);
        this.enteredValue = "";
      }
    },
  },
};
</script>
<style scoped>
div {
  display: flex;
  justify-content: center;
  gap: 2rem;
  align-items: center;
  /* max-width: 120rem;
  margin: 0 auto; */
}
input {
  width: 40rem;
  font-family: inherit;
  padding: 1rem 4rem;
  border-radius: 9px;
  margin-bottom: 2rem;
  /* margin-top: 1rem; */
}
base-button {
  margin-top: 5rem;
}
</style>
