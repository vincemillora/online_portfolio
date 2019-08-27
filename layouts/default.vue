<template>
  <v-app>
    <v-flex v-if="isMobile" pa-5>
      <v-card>
        <v-layout wrap justify-center py-5>
          <v-layout
            column
            fill-height
            align-center
            justify-center>
            <div>
              <v-flex x-12>
                <v-img
                  src="/undraw_under_construction.png"
                  contain
                  height="50vw"
                  width="50vw"
                ></v-img>
              </v-flex>
            </div>
          </v-layout>
          <v-flex px-3 text-xs-center>
          <span class="title">I'm sorry but the Mobile version is still under development. Please re-open the link in a computer.  </span>
          </v-flex>
        </v-layout>
      </v-card>
    </v-flex>
    <v-flex v-else>
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
        class="color-transparent">
        <v-layout 
          column  
          fill-height
          text-xs-center>
          <v-flex
            py-3
            class="primary-color-background white--text">
            <v-layout justify-center>
            <v-flex 
              xs5
              pl-5
              text-xs-left>
              Built with <strong><a class="white--text" @click="openLink('https://nuxtjs.org/')">NUXT.JS</a></strong>.
              Illustrations by <strong><a class="white--text" @click="openLink('https://undraw.co/illustrations')">unDraw</a></strong>.
              Icons from <strong><a class="white--text" @click="openLink('https://fontawesome.com/')">FontAwesome</a></strong>.
            </v-flex>
            <v-flex 
              xs5
              pr-5
              text-xs-right>
              &copy;2019 — <strong>ビンス</strong>
            </v-flex>
            </v-layout>
          </v-flex>
        </v-layout>
      </v-footer>
    </v-flex>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    isMobile: false,
  }),
  mounted() {
    this.isMobile = window.innerWidth < 700;
    window.addEventListener('resize', (() => {
      this.isMobile = window.innerWidth < 700;
    }), { passive: true });
  },
  methods: {
    openLink(link) {
      window.open(link);
    }
  }
}
</script>
