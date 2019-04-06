<template>
  <form  @submit.prevent="handleSubmit">
    <fieldset>
      <details>
        <summary>
          <legend>Part 1</legend>
        </summary>
        <label for="input1">Input 1</label>
        <input type="text" id="input1" name="input1">
      </details>
    </fieldset>
    <fieldset>
      <details>
        <summary>
          <legend>Part 2</legend>
        </summary>
        <label for="input2">Input 2</label>
        <input type="date" id="input2" name="input2">
      </details>
    </fieldset>
    <fieldset>
      <button type="submit">Submit</button>
    </fieldset>
  </form>
</template>

<script>
export default {
  name: "DetailsForm",
  methods: {
    handleSubmit: function (event) {
      
    }
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
