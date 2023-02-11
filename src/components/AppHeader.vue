<template>
  <header>
    <v-system-bar>
      <v-icon icon="mdi-wifi-strength-4"></v-icon>
      <v-icon icon="mdi-signal" class="ms-2"></v-icon>
      <v-icon icon="mdi-battery" class="ms-2"></v-icon>
    
      <span class="ms-2">3:13PM</span>
    </v-system-bar>
    <v-toolbar class="pt-9 pb-3">
        <v-img 
          src="@/assets/afbeeldingen/logo.png"
          alt="logo"
      />
    </v-toolbar>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
};
</script>
