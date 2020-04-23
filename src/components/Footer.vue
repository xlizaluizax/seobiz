<template>
  <footer class="footer">
    <div class="container">
      <span v-html="settings.footer"/>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      settings: require("../../data/theme.json")
    };
  }
};
</script>

<style scoped>
.footer {
  font-size: 1rem;
  padding: 6rem 0;
}
</style>
