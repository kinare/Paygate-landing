<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="/eezy-group.jpg"
          transition="scale-transition"
          width="40"
        />
      </div>

    </v-app-bar>

    <v-main>
      <v-container>
        <v-row>
          <v-col cols="10" offset="1">
            <v-row>
              <v-col md="6" cols="12" class="d-flex mt-5" v-for="(gate, i) in gates" :key="i">
                <v-card color="primary darken-5" dark width="100%" elevation="2" ripple class="py-10" link :href="gate.link" target="_blank">
                    <v-card-text class="text-center">
                      <div style="min-height: 150px;">

                        <v-icon x-large> {{ gate.icon }}</v-icon>

                        <h3 class="text-uppercase text-h2 font-weight-bold overline my-4">
                          {{ gate.name }}
                        </h3>
                        <p class="">{{ gate.description}}</p>
                      </div>
                    </v-card-text>
                  </v-card>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </v-main>

    <v-footer app :inset="true" elevation="12" class="overline">

      <span style="font-size: 0.625rem">
      Paygate © {{ new Date().getFullYear() }}
    </span>

      <v-spacer />

      <v-btn x-small text href="https://kinetics.co.ke/" target="_blank">
        Kinetics Technology LTD
        <v-icon x-small right> mdi-open-in-new </v-icon>
      </v-btn>
    </v-footer>

  </v-app>
</template>

<script>
export default {
  name: 'App',
  computed: {
    gates(){
      return [
        {
          name: "969404",
          link: window.location.protocol + "//" + window.location.hostname +':8080',
          icon: "'mdi-cellphone-wireless",
          description: "Gateway for Eezy Pay bill : 969404",
          color: "indigo"
        },
        {
          name: "969444",
          link: window.location.protocol + "//" + window.location.hostname+':8081',
          icon: "'mdi-cellphone-wireless",
          description: "Gateway for Eezy Pay bill : 969444",
          color: "teal"
        },
        {
          name: "4079527",
          link: window.location.protocol + "//" + window.location.hostname+':8082',
          icon: "'mdi-cellphone-wireless",
          description: "Gateway for Eezy Pay bill : 4079527",
          color: "brown"
        },
        {
          name: "4079511",
          link: window.location.protocol + "//" + window.location.hostname+':8083',
          icon: "'mdi-cellphone-wireless",
          description: "Gateway for Eezy Pay bill : 4079511",
          color: "blue-grey"
        }
      ]
    }
  }
};
</script>
