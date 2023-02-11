<template>
  <v-app>
    <Header />
    <v-main>
      <Dashboard />
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
import Dashboard from "@/components/HomeDashboard";
import Header from "@/components/AppHeader";
import Footer from "@/components/AppFooter";

export default {
  name: "App",

  components: {
    Dashboard,
    Header,
    Footer,
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
