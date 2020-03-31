<template>
  <main id="app" class="container">
    <Header class="row"/>
  </main>
</template>

<script>
import Header from "@/components/HeaderComponent";

export default {
  name: "App",
  components: {
    Header
  }
};
</script>

<style lang="css">
:root {
  --main-text-color: #343a40;
  --main-bg-color: #ededed;
  --container-bg-color: #fff;
}
html,
body {
  background-color: var(--main-bg-color);
  height: 100%;
}
#app {
  font-family: "Roboto", Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  padding: 3em 3em;
  width: 100%;
  height: 100%;
  color: var(--main-text-color);
  background-color: var(--container-bg-color);
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
</style>
