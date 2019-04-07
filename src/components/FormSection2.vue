<template>
  <section>
    <header>{{sectionTitle}}<button>Edit</button></header>
    <fieldset>
      <slot/>
    </fieldset>
  </section>
</template>
<script>
export default {
  name: "FormSection2",
  props: {
    sectionTitle: String
  }
};
</script>

<style scoped>
section:focus-within fieldset {
  display: block;
}
section:not(:focus-within) fieldset {
  display: none;
}
</style>
