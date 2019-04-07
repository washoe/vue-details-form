<template>
  <fieldset>
    <details>
      <summary @click="summaryClicked">
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
    summaryClicked: function() {
      closeOtherDetails(this.$el);
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
