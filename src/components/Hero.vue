<template>
  <div class="hero">
    <h1 class="hero-title" v-html="settings.hero_title"/>
    <h2 class="hero-subtitle" v-html="settings.hero_subtitle"/>
  </div>
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

<style>
.hero {
  text-align: center;
  width: 800px;
  max-width: 100%;
  margin: 0 auto;
  padding: 1.5rem 0 4rem 0;
}

.hero-title {
  font-size: 3rem;
  font-weight: 700px;
  padding: 0;
  margin: 0 0 0rem 0;
}
.hero-title p,
.hero-subtitle p {
  margin: 0 0 0rem 0;
  padding: 0;
}
.hero-subtitle {
  font-size: 1.6rem;
  font-weight: 300;
  line-height: 1.3;
  padding: 0;
  margin: 2;
  opacity: 0.5;
}
</style>
