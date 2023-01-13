<template>
  <div>
    <v-navigation-drawer
      v-model="drawer"
      app
      temporary
      dark
      src="@/assets/img/radio-tower-5949873_960_720.png"
    >
      <v-list>
        <v-list-item>
          <v-list-item-avatar>
            <img src="@/assets/img/logo_maxcom-removebg-preview.png" alt="Logo" />
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-title class="title">Maxcom </v-list-item-title>
            <v-list-item-subtitle>Telecomunicaciones</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </v-list>
      <v-btn
          v-for="(icon, i) in icons"
          :key="i"
          class="mx-3 mb-3 black--text"
          :href="icon.link"
          target="_blank"
          icon
        >
        <v-icon size="35px">{{ icon.text }}</v-icon>
      </v-btn>

      <v-divider />

      <v-list dense>
        <v-list-item
          v-for="([icon, text, link], i) in items"
          :key="i"
          link
          @click="$vuetify.goTo(link)"
        >
          <v-list-item-icon class="justify-center">
            <v-icon>{{ icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="subtitile-1">{{
              text
            }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      app
      :color="color"
      :flat="flat"
      dark
      class="px-15"
      :class="{ expand: flat }"
    >
      <v-toolbar-title>
        <v-img src="@/assets/img/logo_maxcom-removebg-preview.png" width="300px" style="margin-top: 40px;" />
      </v-toolbar-title>
      <v-spacer />
      <v-app-bar-nav-icon
        @click.stop="drawer = !drawer"
        class="mr-4"
        v-if="isXs"
      />
      <div v-else>
        <v-btn rounded outlined text @click="$vuetify.goTo('#hero')">
          <span class="mr-2">Inicio</span>
        </v-btn> 
        <v-btn rounded outlined text @click="$vuetify.goTo('#features')">
          <span class="mr-2">Quienes Somos</span>
        </v-btn>
        <v-btn rounded outlined text @click="$vuetify.goTo('#pricing')">
          <span class="mr-2">Servicios</span>
        </v-btn>
        <v-btn rounded outlined text @click="$vuetify.goTo('#contact')">
          <span class="mr-2">Contactenos</span>
        </v-btn>
        <v-btn
          v-for="(icon, i) in icons"
          :key="i"
          class="mx-0.5 black--text"
          :href="icon.link"
          target="_blank"
          icon
        >
        <v-icon size="35px">{{ icon.text }}</v-icon>
      </v-btn>
      </div>
    </v-app-bar>
  </div>
  
</template>

<style scoped>
.v-toolbar {
  transition: 0.6s;
}

.expand {
  height: 80px !important;
  padding-top: 10px;
}
</style>

<script>
export default {
  data: () => ({
    icons: [
      {
        text: "mdi-facebook",
        link: "https://www.facebook.com/profile.php?id=100064015896229",
      },
      {
        text: "mdi-twitter",
        link: "https://twitter.com/MaxcomTelecomu1",
      },
      {
        text: "mdi-youtube",
        link: "https://www.youtube.com/channel/UCNrnRunHEYm681GPu24VDwQ/featured",
      },
      {
        text: "mdi-instagram",
        link: "https://www.instagram.com/MaxcomTelecomunicaciones/",
      },
    ],
    drawer: null,
    isXs: false,
    items: [
      ["mdi-home-outline", "Inicio", "#hero"],
      ["mdi-information-outline", "Quienes Somos", "#features"],
      ["mdi-currency-usd", "Nuestros Servicios", "#pricing"],
      ["mdi-email-outline", "Contactenos", "#contact"],
    ],
  }),
  props: {
    color: String,
    flat: Boolean,
  },
  methods: {
    onResize() {
      this.isXs = window.innerWidth < 850;
    },
  },

  watch: {
    isXs(value) {
      if (!value) {
        if (this.drawer) {
          this.drawer = false;
        }
      }
    },
  },
  mounted() {
    this.onResize();
    window.addEventListener("resize", this.onResize, { passive: true });
  },
};
</script>
<style scoped>
.v-btn__content span{
  color: black !important;
}

.v-btn {
  background-color: white !important;
  margin-left: 2px;
}
.v-btn--icon.v-size--default .v-icon, .v-btn--fab.v-size--default .v-icon {
  height: 24px;
  font-size: 24px;
  width: 24px;
  color: black;
}
</style>
