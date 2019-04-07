<template>
  <fieldset>
    <details>
      <summary @click="closeOtherDetails">
        <legend>{{sectionTitle}}</legend>
      </summary>
      <slot/>
    </details>
  </fieldset>
</template>

<script>
/**
 * Close all other details elements
 * @param {element} detailsElement to keep open
 * (change event to focus to close other details before opening)
 */
const closeOtherDetails = detailsElement => {
  [...document.querySelectorAll("details[open]")]
    .filter(el => !el.isSameNode(detailsElement))
    .forEach(el => el.removeAttribute("open"));
};
export default {
  name: "FormSection",
  props: {
    sectionTitle: String
  },
  methods: {
    closeOtherDetails: function() {
      closeOtherDetails(this.$el.querySelector('details'));
    }
  }
};
</script>

<style scoped>
summary {
  display: flex;
  align-items: center;
}
</style>
