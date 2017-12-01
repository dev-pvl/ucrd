<template>
  <header class="main-header">
    <button @click.prevent="showSettingsHandler" type="button" name="button" class="settings" >
      Customize
    </button>
  </header>

</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      a: 1,
    };
  },
  methods: {
    showSettingsHandler() {
      this.$parent.showSettings = !this.$parent.showSettings;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
