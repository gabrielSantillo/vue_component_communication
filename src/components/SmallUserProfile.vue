<template>
  <div>
    <h3>Name: {{ user[`name`] }}</h3>
    <h4>Age: {{ user[`age`] }}</h4>
    <p>Is premium: {{user[`is_premium`]}}</p>
  </div>
</template>

<script>
export default {
  props: {
    user: Object,
  },
};
</script>

<style scoped></style>
