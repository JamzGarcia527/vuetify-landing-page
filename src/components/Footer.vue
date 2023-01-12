<template>
  <v-footer dark padless>
    <v-card flat tile class="secondary white--text text-center">
      <v-card-text>
        <v-btn
          v-for="(icon, i) in icons"
          :key="i"
          class="mx-4 white--text"
          :href="icon.link"
          target="_blank"
          icon
        >
          <v-icon size="24px">{{ icon.text }}</v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0">
        Es una compañía contratista de alta reputación en Ciudad San Pedro de Urabá. Desde Nuestro inicio de operaciones, usamos un enfoque integral en todo proyecto, ofreciendo una amplia variedad de servicios para todo tipo de necesidades. 
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong><a href="https://www.facebook.com/kcahzmaj" target="_blank">Desarrollado por Jamz Garcia Development WEB</a></strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<style scoped>
.v-card {
  width: 100%;
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
  }),
};
</script>
