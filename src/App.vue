<template>
  <div id="app">
    <article>
      <small-user-profile v-for="user in users" :key="user[`id`]" :user="user"></small-user-profile>
    </article>
  </div>
</template>

<script>
import SmallUserProfile from "./components/SmallUserProfile.vue";

export default {
  data() {
    return {
      users: [
        {
          name: `Gabriel`,
          age: 26,
          is_premium: true,
          id: `01`,
        },
        {
          name: `Natalia`,
          age: 37,
          is_premium: true,
          id: `02`,
        },
      ],
    };
  },

  name: "App",
  components: {
    SmallUserProfile,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
