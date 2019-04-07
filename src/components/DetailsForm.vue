<template>
<section>
<h1>Collapsible forms</h1>

  <form @submit.prevent="handleSubmit">
    <h2>Using details element and some js</h2>
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
      <select id="input3" name="input3">
        <option>option 1</option>
        <option>option 2</option>
      </select>
    </FormSection>
    <fieldset>
      <button type="submit">Submit</button>
    </fieldset>
  </form>

    <form @submit.prevent="handleSubmit">
    <h2>Using css only</h2>
    <FormSection2 section-title="Part 1">
        <label for="input1">Input 1</label>
        <input type="text" id="input1" name="input1">
    </FormSection2>
    <FormSection2 section-title="Part 2">
        <label for="input2">Input 2</label>
        <input type="date" id="input2" name="input2">
    </FormSection2>
    <FormSection2 section-title="Part 3">
      <label for="input3">Input 3</label>
      <select id="input3" name="input3">
        <option>option 1</option>
        <option>option 2</option>
      </select>
    </FormSection2>
    <fieldset>
      <button type="submit">Submit</button>
    </fieldset>
  </form>
  </section>
</template>

<script>
import FormSection from "./FormSection";
import FormSection2 from "./FormSection2";
export default {
  name: "DetailsForm",
  components: {
    FormSection,
    FormSection2
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
