<template>
  <div @click="user_clicked">
    <h3>Name: {{ user[`name`] }}</h3>
    <h4>Age: {{ user[`age`] }}</h4>
    <p>Is premium: {{user[`is_premium`]}}</p>
  </div>
</template>

<script>
export default {
    methods: {
        user_clicked() {
           this.$emit(`user_clicked`, this.user[`name`]);
        }
    },

  props: {
    user: Object,
  },
};
</script>

<style scoped>
div {
    cursor: pointer;
}
</style>
