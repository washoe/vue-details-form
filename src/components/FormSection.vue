<template>
    <fieldset>
      <details>
        <summary>
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
  }
};
</script>

<style scoped>
summary {
  display: flex;
  align-items: center;
}
</style>
