<template>
  <div class="app-wrapper" id="app">
    <Accordion />
  </div>
</template>

<script>
import Accordion from "./components/Accordion.vue";

export default {
  name: "App",
  components: {
    Accordion,
  },
};
</script>

<style scoped>
.app-wrapper {
  padding: 0;
  margin: 0;
  width: 100vw;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

@media (max-width: 768px) {
  .app-wrapper {
    padding: 32px 8px;
  }
}

@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;800&display=swap");
</style>
