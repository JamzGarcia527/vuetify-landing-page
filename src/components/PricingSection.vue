<template>
  <section id="pricing" class="pb-8">
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-card style="width: 100%">
            <h1 class="text-center pt-6 font-weight-light display-2">
              Nuestros Servicios
            </h1>
            <v-divider class="my-6"></v-divider>
            <v-row class="text-center">
              <v-col class="col-12 col-sm-6 col-md-4">
                <div class="flex-center">
                  <v-card-text>
                    <div class="flex-center">
                      <div class="circle1">
                        <div class="circle2">
                          <v-img
                            src="~@/assets/img/solar-panels-couple-in-sunlight-svgrepo-com.svg"
                          ></v-img>
                        </div>
                      </div>
                    </div>
                    <div class="text--disabled text-uppercase text-h5 my-2">
                      Paneles <br />
                      Solares
                    </div>
                    <v-divider class="my-2" />
                    <div class="text-uppercase blue--text">
                      En Maxcom Telecomunicaciones encontrará todo tipo de
                      paneles solares a precios inmejorables y para diferente
                      usos dentro del mercado de la energía solar.
                    </div>
                    <v-divider class="my-2" />
                    <div class="text-center">
                      <v-dialog v-model="dialog" width="500">
                        <template v-slot:activator="{ on, attrs }">
                          <v-btn
                            color="black lighten-2"
                            dark
                            v-bind="attrs"
                            v-on="on"
                          >
                            Ver Detalle
                          </v-btn>
                        </template>

                        <v-card>
                          <v-card-title class="text-h5 grey lighten-2">
                            Paneles Solares
                          </v-card-title>

                          <v-card-text>
                            Los paneles solares son el intermediario que hace
                            que la luz solar nos sirva de energía. Su diseño es
                            simple, muy eficaz y permite el autoconsumo, lo que
                            fomenta la sostenibilidad. En un futuro próximo, los
                            paneles generarán electricidad incluso de noche.
                          </v-card-text>

                          <v-img
                            src="~@/assets/img/solar-panels-couple-in-sunlight-svgrepo-com.svg"
                            width="200px"
                            height="200px"
                            style="margin-left: 30%"
                          ></v-img>

                          <v-divider></v-divider>

                          <v-card-actions>
                            <v-spacer></v-spacer>
                            <v-btn color="primary" text>
                              <a :href="link" target="_blank">
                                Solicitar Cotización
                              </a>
                            </v-btn>
                            <v-btn color="primary" text @click="closeModal()">
                              Cerrar
                            </v-btn>
                          </v-card-actions>
                        </v-card>
                      </v-dialog>
                    </div>
                  </v-card-text>
                  <v-divider
                    style="margin-right: -23px"
                    vertical
                    v-if="this.$vuetify.breakpoint.smAndUp"
                  ></v-divider>
                </div>
                <v-divider
                  class="mx-4"
                  v-if="!this.$vuetify.breakpoint.smAndUp"
                ></v-divider>
              </v-col>
              <v-col class="col-12 col-sm-6 col-md-4">
                <div class="flex-center">
                  <v-card-text>
                    <div class="flex-center">
                      <div class="circle1">
                        <div class="circle2">
                          <v-img
                            src="~@/assets/img/internet-3-svgrepo-com.svg"
                          />
                        </div>
                      </div>
                    </div>
                    <div class="text--disabled text-uppercase text-h5 my-2">
                      Cable <br />
                      de Datos
                    </div>
                    <v-divider class="my-2" />
                    <div class="text-uppercase blue--text">
                      Conocemos de la importancia y el nivel de exigencia que se
                      requiere en este campo, por ello los diferentes cables de
                      datos con los que trabajamos cumplen con estos requisitos
                    </div>
                    <v-divider class="my-2" />
                    <v-dialog v-model="dialogCableData" width="500">
                      <template v-slot:activator="{ on, attrs }">
                        <v-btn
                          color="black lighten-2"
                          dark
                          v-bind="attrs"
                          v-on="on"
                        >
                          Ver Detalle
                        </v-btn>
                      </template>
                      <v-card>
                        <v-card-title class="text-h5 grey lighten-2">
                          Cable de datos
                        </v-card-title>
                        <v-card-text>
                          El cableado estructurado consiste en el tendido de
                          cables en el interior de un edificio, con el propósito
                          de implantar en un futuro una red de área local. Suele
                          tratarse de cable de par trenzado de cobre UTP/STP,
                          para redes de tipo IEEE 802.3
                          <ul>
                            <li>
                              <h3>Categoria 1</h3>
                              <br />
                              <p>
                                se utiliza para comunicaciones telefónicas y no
                                es adecuado para la transmisión de datos ya que
                                sus velocidades no alcanzan los 512 kbit/s
                              </p>
                            </li>
                            <li>
                              <h3>Categoria 2</h3>
                              <br />
                              <p>
                                puede transmitir datos a velocidades de hasta 4
                                Mbit/s.
                              </p>
                            </li>
                            <li>
                              <h3>Categoria 3</h3>
                              <br />
                              <p>
                                se utiliza en redes 10BaseT y puede transmitir
                                datos a velocidades de hasta 10 Mbit/s.e
                              </p>
                            </li>
                            <li>
                              <h3>Categoria 4</h3>
                              <br />
                              <p>
                                se utiliza en redes Token Ring y puede
                                transmitir datos a velocidades de hasta 16
                                Mbit/s.
                              </p>
                            </li>
                            <li>
                              <h3>Categoria 5</h3>
                              <br />
                              <p>
                                puede transmitir datos a velocidades de hasta
                                100 Mbit/s.
                              </p>
                            </li>
                            <li>
                              <h3>Categoria 6</h3>
                              <br />
                              <p>Redes de alta velocidad hasta 1 Gbit/s.</p>
                            </li>
                            <li>
                              <h3>Categoria 6A</h3>
                              <br />
                              <p>Redes de alta velocidad hasta 10 Gbit/s</p>
                            </li>
                          </ul>
                        </v-card-text>

                        <v-img
                          src="~@/assets/img/18348536081640501793.svg"
                          width="200px"
                          height="200px"
                          style="margin-left: 30%"
                        ></v-img>

                        <v-divider></v-divider>

                        <v-card-actions>
                          <v-spacer></v-spacer>
                          <v-btn color="primary" text>
                            <a :href="linkCableData" target="_blank">
                              Solicitar Cotización
                            </a>
                          </v-btn>
                          <v-btn
                            color="primary"
                            text
                            @click="closeModalCableData()"
                          >
                            Cerrar
                          </v-btn>
                        </v-card-actions>
                      </v-card>
                    </v-dialog>
                  </v-card-text>
                  <v-divider
                    style="margin-right: -23px"
                    vertical
                    v-if="this.$vuetify.breakpoint.mdAndUp"
                  ></v-divider>
                </div>
                <v-divider
                  class="mx-4"
                  v-if="!this.$vuetify.breakpoint.smAndUp"
                ></v-divider>
              </v-col>
              <v-col class="col-12 col-md-4">
                <v-divider
                  v-if="this.$vuetify.breakpoint.smOnly"
                  class="mx-4"
                ></v-divider>
                <div class="flex-center">
                  <v-card-text>
                    <div class="flex-center">
                      <div class="circle1">
                        <div class="circle2">
                          <v-img src="~@/assets/img/3052650321556281130.svg" />
                        </div>
                      </div>
                    </div>
                    <div class="text--disabled text-uppercase text-h5 my-2">
                      Punto de Acceso Inalambrico
                    </div>
                    <v-divider class="my-2" />
                    <div class="text-uppercase blue--text">
                      Un punto de acceso es un dispositivo que crea una red de
                      área local inalámbrica, o WLAN, generalmente en una casa,
                      oficina o en un edificio mucho más grande.
                    </div>
                    <v-divider class="my-2" />
                    <v-dialog v-model="dialogAccessPoint" width="500">
                      <template v-slot:activator="{ on, attrs }">
                        <v-btn
                          color="black lighten-2"
                          dark
                          v-bind="attrs"
                          v-on="on"
                        >
                          Ver Detalle
                        </v-btn>
                      </template>
                      <v-card>
                        <v-card-title class="text-h5 grey lighten-2">
                          Punto de Acceso Inalambrico
                        </v-card-title>
                        <v-card-subtitle class="text-h5 grey lighten-2">
                          ¿Qué es un punto de acceso?
                        </v-card-subtitle>
                        <v-card-text>
                          Un punto de acceso es un dispositivo que crea una red
                          de área local inalámbrica (WLAN), normalmente en una
                          oficina o un edificio de grandes dimensiones.
                        </v-card-text>

                        <v-img
                          src="~@/assets/img/11911825931552562353.svg"
                          width="200px"
                          height="200px"
                          style="margin-left: 30%"
                        ></v-img>

                        <v-divider></v-divider>

                        <v-card-actions>
                          <v-spacer></v-spacer>
                          <v-btn color="primary" text>
                            <a :href="linkAccessPoint" target="_blank">
                              Solicitar Cotización
                            </a>
                          </v-btn>
                          <v-btn
                            color="primary"
                            text
                            @click="closeModalAccessPoint()"
                          >
                            Cerrar
                          </v-btn>
                        </v-card-actions>
                      </v-card>
                    </v-dialog>
                  </v-card-text>
                </div>
              </v-col>
              <v-col class="col-12 col-md-6">
                <v-divider
                  v-if="this.$vuetify.breakpoint.smOnly"
                  class="mx-4"
                ></v-divider>
                <div class="flex-center">
                  <v-card-text>
                    <div class="flex-center">
                      <div class="circle1">
                        <div class="circle2">
                          <v-img src="~@/assets/img/1464653321594941699.svg" />
                        </div>
                      </div>
                    </div>
                    <div class="text--disabled text-uppercase text-h5 my-2">
                      Internet Dedicado <br />
                      y Banda Ancha
                    </div>
                    <v-divider class="my-2" />
                    <div class="text-uppercase blue--text">
                      una línea de Internet Dedicado es una conexión entre dos
                      puntos con un Ancho de Banda fijo, la cual está disponible
                      las 24 horas del día, los 7 días de la semana.
                    </div>
                    <v-divider class="my-2" />
                    <v-dialog v-model="dialogIntBandaAncha" width="500">
                      <template v-slot:activator="{ on, attrs }">
                        <v-btn
                          color="black lighten-2"
                          dark
                          v-bind="attrs"
                          v-on="on"
                        >
                          Ver Detalle
                        </v-btn>
                      </template>

                      <v-card>
                        <v-card-title class="text-h5 grey lighten-2">
                          Internet Dedicado y Banda Ancha
                        </v-card-title>

                        <v-card-text>
                          El Internet dedicado es una conexión desarrollada especialmente para el sector corporativo. 
                          La diferencia entre esta conexión y la banda ancha tradicional es la calidad de navegación. 
                          El Internet dedicado, independientemente del tamaño, garantiza un acceso más seguro, estable y con alta escala.
                        </v-card-text>

                        <v-img
                          src="~@/assets/img/8673964291600702428.svg"
                          width="200px"
                          height="200px"
                          style="margin-left: 30%"
                        ></v-img>

                        <v-divider></v-divider>

                        <v-card-actions>
                          <v-spacer></v-spacer>
                          <v-btn
                            color="primary"
                            text
                          >
                            <a :href="linkIntBandaAncha" target="_blank">
                              Solicitar Cotización
                            </a>
                          </v-btn>
                          <v-btn color="primary" text @click="closeModalIntBandaAncha()">
                            Cerrar
                          </v-btn>
                        </v-card-actions>
                      </v-card>
                    </v-dialog>
                  </v-card-text>
                </div>
              </v-col>
              <v-col class="col-12 col-md-6">
                <v-divider
                  v-if="this.$vuetify.breakpoint.smOnly"
                  class="mx-4"
                ></v-divider>
                <div class="flex-center">
                  <v-card-text>
                    <div class="flex-center">
                      <div class="circle1">
                        <div class="circle2">
                          <v-img src="~@/assets/img/3052650321556281130.svg" />
                        </div>
                      </div>
                    </div>
                    <div class="text--disabled text-uppercase text-h5 my-2">
                      Internet <br />
                      Hostpot
                    </div>
                    <v-divider class="my-2" />
                    <div class="text-uppercase blue--text">
                      Se trata del acceso de cobertura que se ofrece a través de
                      un dispositivo para que haya una comunicación inalámbrica,
                      sin cables, WIFI.
                    </div>
                    <v-divider class="my-2" />
                    <v-dialog v-model="dialogHostPot" width="500">
                      <template v-slot:activator="{ on, attrs }">
                        <v-btn
                          color="black lighten-2"
                          dark
                          v-bind="attrs"
                          v-on="on"
                        >
                          Ver Detalle
                        </v-btn>
                      </template>

                      <v-card>
                        <v-card-title class="text-h5 grey lighten-2">
                          Internet HostPot
                        </v-card-title>

                        <v-card-text>
                          Los hotspots WiFi son puntos de acceso a Internet que te permiten conectarte a una red WiFi utilizando tu computadora,
                           smartphone u otro dispositivo cuando estás lejos de tu red residencial o de la de tu oficina. 
                           Muchas ciudades, empresas y otras organizaciones han comenzado a ofrecer hotspots WiFi para uso público.
                        </v-card-text>

                        <v-img
                          src="~@/assets/img/8673964291600702428.svg"
                          width="200px"
                          height="200px"
                          style="margin-left: 30%"
                        ></v-img>

                        <v-divider></v-divider>

                        <v-card-actions>
                          <v-spacer></v-spacer>
                          <v-btn
                            color="primary"
                            text
                          >
                            <a :href="linkHostPot" target="_blank">
                              Solicitar Cotización
                            </a>
                          </v-btn>
                          <v-btn color="primary" text @click="closeModalHostPot()">
                            Cerrar
                          </v-btn>
                        </v-card-actions>
                      </v-card>
                    </v-dialog>
                  </v-card-text>
                </div>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
    <div class="svg-border-rounded text-light">
      <!-- <svg
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 144.54 17.34"
        preserveAspectRatio="none"
        fill="currentColor"
      >
        <path
          d="M144.54,17.34H0V0H144.54ZM0,0S32.36,17.34,72.27,17.34,144.54,0,144.54,0"
        />
      </svg> -->
      <svg
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 1440 320"
        preserveAspectRatio="none"
        fill="currentColor"
      >
        <path
          d="M0,64L80,90.7C160,117,320,171,480,181.3C640,192,800,160,960,138.7C1120,117,1280,107,1360,101.3L1440,96L1440,320L1360,320C1280,320,1120,320,960,320C800,320,640,320,480,320C320,320,160,320,80,320L0,320Z"
        ></path>
      </svg>
    </div>
  </section>
</template>

<style lang="scss">
$main_color: #283e79;

ul {
  font-size: 13px;
  line-height: 1.5em;
  margin: 5px 0 15px;
  padding: 0;

  li {
    list-style: none;
    position: relative;
    padding: 0 0 0 20px;
  }

  li {
    &::before {
      content: "";
      position: absolute;
      left: 0;
      top: 5px;
      width: 10px;
      height: 10px;
      background-color: $main_color;
      border-radius: 50%;
      -moz-border-radius: 50%;
      -webkit-eeborder-radius: 50%;
    }
  }
}
</style>

<style scoped>
.header {
  background-color: #283e79;
  color: white;
}

.circle1 {
  border-radius: 50%;
  width: 150px;
  height: 150px;
  background-color: #f0f8ff;
  display: flex;
  align-items: center;
  justify-content: center;
}

.circle2 {
  border-radius: 50%;
  width: 100px;
  height: 100px;
  background-color: #e0effc;
  display: flex;
  align-items: center;
  justify-content: center;
}

.flex-center {
  display: flex;
  align-items: center;
  justify-content: center;
}

.svg-border-rounded svg {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  color: #f4f7f5;
  z-index: -1;
}

#pricing {
  z-index: 0;
}

.content {
  z-index: 1;
}

svg {
  overflow: hidden;
}

section {
  position: relative;
}
</style>

<script>
import Swal from "sweetalert";
export default {
  data: () => ({
    dialog: false,
    dialogCableData: false,
    dialogAccessPoint: false,
    dialogIntBandaAncha: false,
    dialogHostPot: false,
    linkHostPot: 'https://wa.link/3n0jpq',
    linkIntBandaAncha: 'https://wa.link/ik7sp2',
    linkAccessPoint: "https://wa.link/k81kdd",
    linkCableData: "https://wa.link/ojzsyt",
    link: "https://wa.link/8b4ddc",
  }),
  computed: {
    size() {
      const size = { md: "large", xl: "x-large" }[
        this.$vuetify.breakpoint.name
      ];
      return size ? { [size]: true } : {};
    },
  },
  methods: {
    closeModal() {
      this.dialog = false;
    },
    closeModalCableData() {
      this.dialogCableData = false;
    },
    closeModalAccessPoint() {
      this.dialogAccessPoint = false;
    },
    closeModalIntBandaAncha() {
      this.dialogIntBandaAncha = false;
    },
    closeModalHostPot() {
      this.dialogHostPot = false;
    },

    
  },
};
</script>
