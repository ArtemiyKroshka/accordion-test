<template>
  <div class="accordion">
    <div v-for="(accordion, key) in accordionText" :key="key">
      <AccordionBlock :accordion="accordion" />
    </div>
  </div>
</template>

<script>
import AccordionBlock from "./AccordionBlock.vue";

export default {
  name: "AccordionWrapper",
  components: { AccordionBlock },
  data() {
    return {
      accordionText: [
        {
          title: "The analysis",
          text: [
            "Do you have one user in more than one variant of the same AB test?",
            "Are you users actually getting the treatment we expect them to get?",
            "Do we have enough users in our AB test? Are those users representative for the total population?",
          ],
        },
        {
          title: "To take into account on user level data",
          text: [
            "Do you have one user in more than one variant of the same AB test?",
            "Are you users actually getting the treatment we expect them to get?",
            "Do we have enough users in our AB test? Are those users representative for the total population?",
          ],
        },
        {
          title: "Our data",
          text: [
            "Do you have one user in more than one variant of the same AB test?",
            "Are you users actually getting the treatment we expect them to get?",
            "Do we have enough users in our AB test? Are those users representative for the total population?",
          ],
        },
        {
          title: "Our study case",
          text: [
            "Do you have one user in more than one variant of the same AB test?",
            "Are you users actually getting the treatment we expect them to get?",
            "Do we have enough users in our AB test? Are those users representative for the total population?",
          ],
        },
        {
          title: "Hands or analyzing",
          text: [
            "Do you have one user in more than one variant of the same AB test?",
            "Are you users actually getting the treatment we expect them to get?",
            "Do we have enough users in our AB test? Are those users representative for the total population?",
          ],
        },
        {
          title: "Initialization",
          text: [
            "Do you have one user in more than one variant of the same AB test?",
            "Are you users actually getting the treatment we expect them to get?",
            "Do we have enough users in our AB test? Are those users representative for the total population?",
          ],
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.accordion {
  width: 600px;
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.02), 0px 4px 17px rgba(0, 0, 0, 0.14),
    0px 4px 22px rgba(0, 0, 0, 0.12);
  border-radius: 8px;
}

.accordion div:last-child .accordion-block {
  border-bottom: none;
}

@media (max-width: 768px) {
  .accordion {
    width: 60vh;
  }
}

@media (max-width: 420px) {
  .accordion {
    width: 100%;
  }
}
</style>
