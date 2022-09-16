<template>
  <header class="header-wrapper">
    <h1>{{ title }}</h1>
  </header>
</template>
<script>
export default {
  data() {
    return {};
  },
  props: ["title"],
};
</script>
<style scoped>
.header-wrapper {
  max-width: 120rem;
  background-color: #005e2dd8;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 1.6rem 0;
}
h1 {
  font-size: 4.4rem;
  font-weight: 700;
  color: #fff;
}
</style>
