<template>
  <v-app>
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
          class="secondary-color-background">
          <v-layout 
            wrap
            justify-center>
            <v-flex 
              xs12
              sm6
              text-sm-left
              text-xs-center
              :pl-5="!this.$vuetify.breakpoint.xs"
              class="white--text">
              <span v-if="$i18n.locale === 'en'">
                Built with <strong><a class="white--text" @click="openLink('https://nuxtjs.org/')">NUXT.JS</a></strong>.
                Illustrations by <strong><a class="white--text" @click="openLink('https://undraw.co/illustrations')">unDraw</a></strong>.
                Icons from <strong><a class="white--text" @click="openLink('https://fontawesome.com/')">FontAwesome</a></strong>.
              </span>
              <span v-else>
                <strong><a class="white--text" @click="openLink('https://nuxtjs.org/')">NUXT.JS</a></strong>で構築。
                <strong><a class="white--text" @click="openLink('https://undraw.co/illustrations')">unDraw</a></strong>からの絵。
                <strong><a class="white--text" @click="openLink('https://fontawesome.com/')">FontAwesome</a></strong>のアイコン。
              </span>
            </v-flex>
            <v-flex 
              xs12
              sm6
              text-sm-right
              text-xs-center
              :pr-5="!this.$vuetify.breakpoint.xs"
              :pt-2="this.$vuetify.breakpoint.xs"
              class="white--text">
              &copy;2019 — <strong>ビンス</strong>
            </v-flex>
          </v-layout>
        </v-flex>
      </v-layout>
    </v-footer>
  </v-app>
</template>

<script>
import AOS from 'aos';
import 'aos/dist/aos.css';

export default {
  props: ['error'],
  mounted() {
    AOS.init();
  },
  methods: {
    openLink(link) {
      window.open(link);
    },
  }
}
</script>
