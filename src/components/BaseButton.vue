<template>
  <div>
    <button>
      <slot></slot>
    </button>
  </div>
</template>
<script>
export default {};
</script>
<style scoped>
button {
  border: none;
  font-weight: 700;
  font-size: 1.8rem;
  padding: 0.5rem 1rem;
  margin-bottom: 2rem;
  color: #fff;
  background-color: #005e2dd8;
  text-transform: uppercase;
  cursor: pointer;
  transition: all 0.3s;
}
button:hover,
button:active {
  background-color: #35885ddb;
  transform: translateY(-20%);
}
</style>
