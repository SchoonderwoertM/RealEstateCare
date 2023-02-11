<template>
  <v-app>
    <AppHeader />
    <v-main>
      <HelloWorld />
    </v-main>
    <AppFooter />
  </v-app>
</template>

<script>
import HelloWorld from "@/components/HelloWorld";
import AppHeader from "@/components/AppHeader";
import AppFooter from "@/components/AppFooter";

export default {
  name: "App",

  components: {
    HelloWorld,
    AppHeader,
    AppFooter,
  },

  data: () => ({
    //
  }),
};
</script>

<style>
@import "@/assets/css/main.css";

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #293439;
}
</style>
