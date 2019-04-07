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
export default {
  name: "FormSection",
  props: {
    sectionTitle: String
  },
  methods: {
    summaryClicked: event => {
      // Close all other details elements
      [...document.querySelectorAll("details[open]")]
        .filter(el => el.querySelector("summary") !== event.target)
        .forEach(el => el.removeAttribute("open"));
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
