<template>
  <v-app>
    <v-toolbar
      color="transparent"
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
              <svg height="40" width="100">
                <rect id="shape" height="40" width="100"/>
                <text x="50%" y="70%" class="subheading custom-button-svg-text font-weight-light">Work</text>
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
              <svg height="40" width="100">
                <rect id="shape" height="40" width="100"/>
                <text x="50%" y="70%" class="subheading custom-button-svg-text font-weight-light">About</text>
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
              <svg height="40" width="100">
                <rect id="shape" height="40" width="100"/>
                <text x="50%" y="75%" class="headline custom-button-svg-text font-weight-bold">ビンス</text>
              </svg>
            </div>
          </v-btn>
        </v-flex>
      </v-layout>
    </v-toolbar>
    <v-content>
      <v-container>
        <nuxt/>
      </v-container>
    </v-content>
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
