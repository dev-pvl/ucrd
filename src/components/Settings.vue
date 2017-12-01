<template>
  <aside class="settings">
    <h1>Main settings</h1>
  </aside>

</template>

<script>
export default {
  name: 'Settings',
  data() {
    return {
      msg: 'Welcome to Your Vue.js App',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .settings {
    position: absolute;
    top: 0;
    right: 0;
    width: 400px;
    height: 100vh;
  }
</style>
