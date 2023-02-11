<template>
  <v-container style="max-width:1000px">
    <v-row>
      <v-col cols="6">
        <v-hover v-slot="{ isHovering, props }">
          <v-card
            :elevation="isHovering ? 16 : 5"
            :class="{ 'on-hover': isHovering }"
            height="35vh"
            class="d-flex align-center justify-center"
            v-bind="props"
          >
            <v-icon size="150" class="pl-10 pr-10">mdi-clipboard-edit</v-icon>
          </v-card>
        </v-hover>
      </v-col>
      <v-col cols="6">
        <v-hover v-slot="{ isHovering, props }">
          <v-card
            :elevation="isHovering ? 16 : 5"
            :class="{ 'on-hover': isHovering }"
            height="35vh"
            class="d-flex align-center justify-center"
            v-bind="props"
          >
            <v-icon size="150">mdi-clipboard-check</v-icon>
          </v-card>
        </v-hover>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="6">
        <v-hover v-slot="{ isHovering, props }">
          <v-card
            :elevation="isHovering ? 16 : 5"
            :class="{ 'on-hover': isHovering }"
            height="35vh"
            class="d-flex align-center justify-center"
            v-bind="props"
          >
            <v-icon size="150">mdi-folder</v-icon>
          </v-card>
        </v-hover>
      </v-col>
      <v-col cols="6">
        <v-hover v-slot="{ isHovering, props }">
          <v-card
            :elevation="isHovering ? 16 : 5"
            :class="{ 'on-hover': isHovering }"
            height="35vh"
            class="d-flex align-center justify-center"
            v-bind="props"
          >
            <v-icon size="150">mdi-cog</v-icon>
          </v-card>
        </v-hover>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",
};
</script>
