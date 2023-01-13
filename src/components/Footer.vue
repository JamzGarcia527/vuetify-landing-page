<template>
  <v-footer dark padless>
    <v-card flat tile class="secondary white--text text-center">
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
    
  }),
};
</script>
