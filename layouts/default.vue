<template>
  <v-app>
    <v-toolbar
      color="transparent"
      absolute=true
      height="100vh"
      fixed
      flat
      app>
      <v-layout class="header">
        <v-flex 
          text-xs-left
          xs6>
          <v-btn
            flat
            nuxt
            to="/"
            class="px-0"
            color="transparent">
            <div class="custom-button-svg-wrapper">
              <svg 
                height="40" 
                width="100">
                <rect 
                  id="shape" 
                  height="40" 
                  width="100"/>
                <text 
                  x="50%" 
                  y="70%" 
                  class="subheading custom-button-svg-text font-weight-light">
                  Work
                </text>
              </svg>
            </div>
          </v-btn>
          <v-btn
            flat
            nuxt
            to="/about"
            class="px-0"
            color="transparent">
            <div class="custom-button-svg-wrapper">
              <svg 
                height="40" 
                width="100">
                <rect 
                  id="shape" 
                  height="40" 
                  width="100"/>
                <text 
                  x="50%" 
                  y="70%" 
                  class="subheading custom-button-svg-text font-weight-light">
                  About
                </text>
              </svg>
            </div>
          </v-btn>
        </v-flex>
        <v-flex 
          text-xs-right
          xs6>
          <v-btn
            flat
            nuxt
            to="/"
            class="px-0"
            color="transparent">
            <div class="custom-button-svg-wrapper">
              <svg 
                height="40" 
                width="100">
                <rect 
                  id="shape" 
                  height="40" 
                  width="100"/>
                <text 
                  x="50%" 
                  y="75%" 
                  class="headline custom-button-svg-text font-weight-bold">
                  ビンス
                </text>
              </svg>
            </div>
          </v-btn>
        </v-flex>
      </v-layout>
    </v-toolbar>
    <v-content>
      <nuxt/>
    </v-content>
    <v-footer
      dark
      height="auto">
      <v-card
        class="flex"
        flat
        tile>
        <v-card-title class="teal">
          <strong class="subheading">Get connected with us on social networks!</strong>

          <v-spacer></v-spacer>

          <v-btn
            v-for="icon in icons"
            :key="icon"
            class="mx-3"
            dark
            icon>
            <v-icon size="24px">{{ icon }}</v-icon>
          </v-btn>
        </v-card-title>
        <v-card-actions class="grey darken-3 justify-center">
          &copy;2018 — <strong>Vuetify</strong>
        </v-card-actions>
      </v-card>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
    }
  }
}
</script>
