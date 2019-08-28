<template>
  <v-layout
    column
    justify-center
    align-center>
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
                <span class="display-2">Software Developer, Creative Thinker, Learner.🤓</span> <br/> <br/> <br/>
                <span class="title primary-color font-weight-regular">I'm a web and systems developer, and a computer games enthusiast.</span>
                <v-img
                  style="margin-top: 25px"
                  v-if="this.$vuetify.breakpoint.xs"
                  src="/undraw_code_review.png"
                  contain
                  width="100%"
                ></v-img>
              </v-flex>
              <v-flex
                xs12
                sm4
                data-aos="fade-left"
                data-aos-duration="1000"
                data-aos-once="false"
                data-aos-mirror="true">
                <v-img
                  v-if="!this.$vuetify.breakpoint.xs"
                  src="/undraw_code_review.png"
                  contain
                  width="50vw"
                ></v-img>
              </v-flex>
          </v-layout>
        </v-flex>
        <v-flex 
          xs12
          py-5
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
import AOS from 'aos';
import 'aos/dist/aos.css';

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
    }
  },
  mounted() {
    AOS.init();
    this.isMobile = window.innerWidth < 600;

    if(window.innerWidth < 600) {
      this.src = '/prof_pic.jpg'
    } else {
      this.src = '/about_me.jpg'
    }
    
    window.addEventListener('resize', () => {
      if(window.innerWidth < 600) {
        this.src = '/prof_pic.jpg'
      } else {
        this.src = '/about_me.jpg'
      }
    }, { passive: true })
  },
}
</script>
