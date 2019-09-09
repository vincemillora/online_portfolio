<template>
  <v-layout>
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
    <v-flex>
      <v-layout wrap>
        <v-flex 
          xs12 
          sm8
          class="whole-page web-component">
          <v-layout
            wrap
            fill-height
            align-center>
              <v-flex 
                xs12
                sm8
                text-xs-center
                text-sm-left
                data-aos="fade-right"
                data-aos-duration="1000"
                data-aos-once="false"
                data-aos-mirror="true">
                <span class="display-2">{{ $t("intro_title") }}🤓 </span> <br/> <br/> <br/>
                <span class="title primary-color">{{ $t("intro_subtitle") }}</span>
                <v-img
                  style="margin-top: 25px"
                  v-if="this.$vuetify.breakpoint.xs"
                  src="/undraw_code_review.png"
                  contain
                  width="100%"
                ></v-img>
              </v-flex>
              <v-flex
                v-if="!this.$vuetify.breakpoint.xs"
                xs12
                sm4
                :data-aos="animation"
                data-aos-duration="1000"
                data-aos-once="false"
                data-aos-mirror="true">
                <v-img
                  src="/undraw_code_review.png"
                  contain
                  width="50vw"
                ></v-img>
              </v-flex>
          </v-layout>
        </v-flex>
        <v-flex 
          xs12
          my-5
          data-aos="fade-up"
          data-aos-duration="1000"
          data-aos-once="false">
          <v-img
            :src="src"
            width="100%"/>
        </v-flex>
      </v-layout>
      <About id="about"/>
      <Project id="project"/>
      <Contact id="contact"/>
    </v-flex>
  </v-layout>
</template>

<script>
import Logo from '~/components/Logo.vue';
import VuetifyLogo from '~/components/VuetifyLogo.vue';
import Contact from '~/pages/contact';
import About from '~/pages/about';
import Project from '~/pages/project';


export default {
  components: {
    Logo,
    VuetifyLogo,
    Contact,
    About,
    Project,
  },
  data() {
    return {
      src: '',
      animation:'fade-left',
    }
  },
  computed: {
    otherLang() {
      return this.$i18n.locale == 'ja' ? 'en' : 'ja';
    }
  },
  mounted() {
    if(window.innerWidth < 960) {
      this.src = '/prof_pic.jpg'
      this.animation = 'fade-right';
    } else {
      this.src = '/about_me.jpg'
    }
    
    window.addEventListener('resize', () => {
      if(window.innerWidth < 960) {
        this.src = '/prof_pic.jpg'
        this.animation = 'fade-right';
      } else {
        this.src = '/about_me.jpg'
        this.animation = 'fade-left';
      }
    }, { passive: true })
  },
  methods: {
    changeLang() {
      const router = this.$router;
      this.$store.dispatch('changeLang', { router, lang: this.otherLang })
    }
  }
}
</script>
