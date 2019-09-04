<template>
  <v-app>
    <v-toolbar
      color="transparent"
      absolute
      fixed
      flat>
      <v-layout           
        wrap
        class="header">
        <v-flex 
          v-if="!this.$vuetify.breakpoint.xs && !this.$vuetify.breakpoint.sm"
          sm12
          md6
          text-sm-left>
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
                  {{ $t('about') }} 
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
                  {{ $t("project") }} 
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
                  {{ $t("contact") }} 
                </text>
              </svg>
            </div>
          </v-btn>
        </v-flex>
        <v-flex 
          xs12
          md6
          text-md-right
          text-xs-center>
          <v-btn
            flat
            nuxt
            @click="changeLang"
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
                  {{ $t('lang') }} 
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
          <v-layout 
            wrap
            justify-center>
            <v-flex 
              xs12
              sm6
              text-sm-left
              text-xs-center
              :pl-5="!this.$vuetify.breakpoint.xs"
              >
              Built with <strong><a class="white--text" @click="openLink('https://nuxtjs.org/')">NUXT.JS</a></strong>.
              Illustrations by <strong><a class="white--text" @click="openLink('https://undraw.co/illustrations')">unDraw</a></strong>.
              Icons from <strong><a class="white--text" @click="openLink('https://fontawesome.com/')">FontAwesome</a></strong>.
            </v-flex>
            <v-flex 
              xs12
              sm6
              text-sm-right
              text-xs-center
              :pr-5="!this.$vuetify.breakpoint.xs"
              :pt-2="this.$vuetify.breakpoint.xs">
              &copy;2019 — <strong>ビンス</strong>
            </v-flex>
          </v-layout>
        </v-flex>
      </v-layout>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  computed: {
    otherLang() {
      return this.$i18n.locale == 'ja' ? 'en' : 'ja';
    }
  },
  methods: {
    openLink(link) {
      window.open(link);
    },
    changeLang() {
      const router = this.$router;
      this.$store.dispatch('changeLang', { router, lang: this.otherLang })
    }
  }
}
</script>
