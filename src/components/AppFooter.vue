<template>
  <v-card>
    <v-tabs fixed-tabs stacked v-model="tab">
      <v-tab value="tab-search">
        <v-icon>mdi-magnify</v-icon>
        search
      </v-tab>
      <v-tab value="tab-notification">
        <v-icon>mdi-bell-outline</v-icon>
        notifications
      </v-tab>
    </v-tabs>
  </v-card>
  <v-footer>
    <v-col class="text-center" cols="12">
      {{ new Date().getFullYear() }} — <strong>Real Estate Care</strong>
    </v-col>
  </v-footer>
</template>

<script>
export default {
  name: "AppFooter",
};
</script>

<style scoped>
.v-footer {
  color: white;
  max-height: 75px;
}
</style>
