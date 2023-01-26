<template>
    <AppHeader />
    <HelloWorld msg="Hello World" />
    <AppFooter />
</template>

<script>
import AppHeader from "@/components/AppHeader.vue";
import HelloWorld from "@/components/HelloWorld.vue";
import AppFooter from "@/components/AppFooter.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    HelloWorld,
    AppFooter,
  },
};
</script>

<style>
@import '@/assets/css/main.css';

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #293439;
}
</style>
