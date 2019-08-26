<template>
  <v-app>
    <v-toolbar
      color="transparent"
      absolute
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
            href="#about"
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
                  About Me
                </text>
              </svg>
            </div>
          </v-btn>
          <v-btn
            flat
            nuxt
            href="#project"
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
                  Projects
                </text>
              </svg>
            </div>
          </v-btn>
          <v-btn
            flat
            nuxt
            href="#contact"
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
                  Contact Me
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
      class="color-transparent"
      height="12vh">
      <v-layout 
        column  
        fill-height
        text-xs-center>
        <v-flex xs8>
          <v-btn 
            fab
            depressed
            class="social-button-wrapper"
            href="https://www.facebook.com/vince.millora"
            target="_blank">
            <span 
              class="title"
              id="icon">
              <font-awesome-icon  
                :icon="['fab', 'facebook-f']"/>
            </span>
          </v-btn>
          <v-btn 
            fab
            depressed
            class="social-button-wrapper"
            href="https://twitter.com/VinceMillora"
            target="_blank">
            <span 
              class="title"
              id="icon">
              <font-awesome-icon  
                :icon="['fab', 'twitter']"/>
            </span>
          </v-btn>
          <v-btn 
            fab
            depressed
            class="social-button-wrapper"
            href="https://www.instagram.com/vcmillora/"
            target="_blank">
            <span 
              class="title"
              id="icon">
              <font-awesome-icon  
                :icon="['fab', 'instagram']"/>
            </span>
          </v-btn>
          <v-btn 
            fab
            depressed
            class="social-button-wrapper"
            href="https://www.linkedin.com/in/vince-millora-3606a0143/"
            target="_blank">
            <span 
              class="title"
              id="icon">
              <font-awesome-icon  
                :icon="['fab', 'linkedin-in']"/>
            </span>
          </v-btn>
          <v-btn 
            fab
            depressed
            class="social-button-wrapper"
            href="https://github.com/vincemillora"
            target="_blank">
            <span 
              class="title"
              id="icon">
              <font-awesome-icon  
                :icon="['fab', 'github']"/>
            </span>
          </v-btn>
          <v-btn 
            fab
            depressed
            class="social-button-wrapper"
            href="https://qiita.com/Binsu"
            target="_blank">
            <span 
              class="title"
              id="icon">
              <font-awesome-icon  
                :icon="['fas', 'newspaper']"/>
            </span>
          </v-btn>
          <v-btn 
            fab
            depressed
            class="social-button-wrapper"
            to="/contact">
            <span 
              class="title"
              id="icon">
              <font-awesome-icon  
                :icon="['fas', 'envelope']"/>
            </span>
          </v-btn>
        </v-flex>
        <v-flex
          class="primary-color-background"
          justify-center
          text-xs-center
          white--text
          py-2
          xs4>
          &copy;2019 — <strong>ビンス</strong>
        </v-flex>
      </v-layout>
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
