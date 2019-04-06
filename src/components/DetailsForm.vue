<template>
  <form @submit.prevent="handleSubmit">
    <FormSection section-title="Part 1">
        <label for="input1">Input 1</label>
        <input type="text" id="input1" name="input1">
    </FormSection>
    <FormSection section-title="Part 2">
        <label for="input2">Input 2</label>
        <input type="date" id="input2" name="input2">
    </FormSection>
    <FormSection section-title="Part 3">
      <label for="input3">Input 3</label>
      <input type="date" id="input3" name="input3">
    </FormSection>
    <fieldset>
      <button type="submit">Submit</button>
    </fieldset>
  </form>
</template>

<script>
import FormSection from "./FormSection";
export default {
  name: "DetailsForm",
  components: {
    FormSection
  },
  methods: {
    handleSubmit: function() {}
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
summary {
  display: flex;
  align-items: center;
}
</style>
