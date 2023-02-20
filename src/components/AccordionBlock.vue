<template>
  <div class="accordion-block" :class="{ open: isOpen }">
    <div :class="{ open: isOpen }" class="accordion-header">
      <span>{{ accordion.title }}</span>
      <button @click="isOpen = !isOpen">
        <i class="fa fa-angle-down" style="font-size: 36px"></i>
      </button>
    </div>
    <div v-if="isOpen" class="accordion-body">
      <div
        class="accordion-body__text"
        v-for="(text, key) in accordion.text"
        :key="key"
      >
        <span>{{ text }}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AccordionBlock",
  props: {
    accordion: {
      type: Object,
    },
  },
  data() {
    return {
      isOpen: false,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.accordion-block {
  width: 100%;
  border-bottom: 1px solid #d0dbf1;
}

.accordion-block.open {
  background-color: #faf8f6;
}
.accordion-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 24px;
}

.accordion-header.open {
  padding-bottom: 0;
}

.accordion-header span {
  font-family: "Montserrat";
  font-size: 16px;
  line-height: 24px;
  font-weight: 800;
  color: #0d2a54;
}

.accordion-header button {
  background-color: transparent;
  outline: none;
  border: none;
  cursor: pointer;
  color: #0d2a54;
}
.accordion-header.open span {
  color: #2b41b7;
}

.accordion-header.open button {
  color: #2b41b7;
  transform: rotate(180deg);
}

.accordion-body {
  padding: 0 44px 24px 60px;
}

.accordion-body__text {
  position: relative;
  margin: 8px;
  font-family: "Montserrat";
  font-weight: 600;
  font-size: 14px;
  line-height: 24px;
  color: #0d2a54;
}

.accordion-body__text span::before {
  content: "";
  position: absolute;
  width: 8px;
  height: 8px;
  border: 2px solid #2b41b7;
  border-radius: 25px;
  top: 6px;
  left: -25px;
}

@media (max-width: 460px) {
  .accordion-header {
    padding: 16px;
  }

  .accordion-body {
    padding: 0 36px 0 16px;
  }

  .accordion-body__text span::before {
    left: -17px;
  }
}
</style>
