<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-back-button
          slot="start"
          :default-href="pageDefaultBackLink"
        ></ion-back-button>
        <ion-img
          src="/logo.png"
          alt="logo"
          class="logo ion-padding"
          @click="goHome"
        />
        <ion-button
          id="logoutButton"
          color="primary"
          slot="end"
          aria-label="uitloggen"
          @click="logout()"
        >
          <ion-icon
            :icon="logOutOutline"
            slot="icon-only"
            aria-hidden="true"
          ></ion-icon>
        </ion-button>
      </ion-toolbar>
    </ion-header>
    <ion-content class="ion-padding">
      <slot />
    </ion-content>
    <ion-footer>
      <ion-toolbar class="ion-padding-start ion-padding-end">
        <ion-buttons id="footerButtons">
          <router-link to="/notifications">
            <ion-button class="footerIcons">
              <ion-icon
                :icon="notificationsOutline"
                slot="icon-only"
              ></ion-icon>
            </ion-button>
          </router-link>
          <router-link to="/home">
            <ion-button class="footerIcons">
              <ion-icon :icon="homeOutline" slot="icon-only"></ion-icon>
            </ion-button>
          </router-link>
          <router-link to="/contact">
            <ion-button class="footerIcons">
              <ion-icon :icon="callOutline" slot="icon-only"></ion-icon>
            </ion-button>
          </router-link>
        </ion-buttons>
      </ion-toolbar>
    </ion-footer>
  </ion-page>
</template>

<script>
import dataBase from '@/data/db.json';
import {
  homeOutline,
  callOutline,
  notificationsOutline,
  logOutOutline,
} from "ionicons/icons";
import {
  IonPage,
  IonContent,
  IonHeader,
  IonToolbar,
  IonTitle,
  IonFooter,
  IonButtons,
  IonButton,
  IonImg,
  IonBackButton,
  IonLabel,
  IonIcon,
} from "@ionic/vue";

export default {
  props: ["pageTitle", "pageDefaultBackLink"],
  components: {
    IonPage,
    IonContent,
    IonHeader,
    IonToolbar,
    IonTitle,
    IonFooter,
    IonButtons,
    IonButton,
    IonImg,
    IonBackButton,
    IonLabel,
    IonIcon,
  },
  setup() {
    return {
      homeOutline,
      callOutline,
      notificationsOutline,
      logOutOutline,
    };
  },
  methods: {
    goHome() {
      this.$router.replace("/home");
    },
    logout() {
      const options = {
        method: "PUT",
        headers: {
          "Content-Type": "application/json",
          "X-Master-Key":
            "$2b$10$xGY57xK/yyF20/AcOpvLJuWh3MnrWeuQZG60ykSCOe49wS5oQ0tw.",
        },
        body: JSON.stringify(dataBase),
      };
      fetch("https://api.jsonbin.io/v3/b/648ed6fc8e4aa6225eb0471c", options);
      this.$store.commit("SET_USER", "");
      sessionStorage.setItem("Authenticated", false);
      this.$router.replace("/login");
    },
  },
};
</script>
