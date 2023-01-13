<template>
  <section id="about">
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="center">
            <v-col cols="12" md="7">
              <h1 class="font-weight-light display-2 text-center">Quienes Somos</h1>
              <hr />
              <v-row>
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="@/assets/img/history-log-manuscript-svgrepo-com.svg"
                    max-width="60px"
                    class="mr-4"
                  />
                  <p class="text-justify mt-3">
                    Maxcom Telecomunicaciones es una compañía contratista de alta reputación en Ciudad San Pedro de Urabá. 
                    Desde Nuestro inicio de operaciones, usamos un enfoque integral en todo proyecto, 
                    ofreciendo una amplia variedad de servicios para todo tipo de necesidades. 
                  </p>
                </v-col>
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="@/assets/img/goal-success-svgrepo-com.svg" 
                    
                    max-width="60px"
                    class="mr-4"
                  />
                  <p class="text-justify ">
                    Misión: Ofrecer a nuestros clientes los mejores productos con la más reciente tecnología. <br />
                  </p>
                </v-col>
                
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="@/assets/img/vision-svgrepo-com.svg"
                    max-width="60px"
                    class="mr-4"
                  />
                  <p class="text-justify ">
                    Visión: Ser la mejor empresa en tecnología del país.
                  </p>
                </v-col>
              </v-row>
            </v-col>
            <v-col cols="12" md="5" class="d-none d-md-flex">
              <v-img
                src="@/assets/img/satellite-2528833.jpg"
                class="d-block ml-auto mr-auto"
                max-width="400px"
              />
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<style scoped>
#about {
  background-color: #f4f7f5;
}
</style>
