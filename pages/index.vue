<template>
  <v-layout
    column
    justify-center
    align-center>
    <v-flex
      xs12
      sm8
      md6>
      <v-layout wrap>
        <v-flex class="web-component whole-page">
          <v-layout>
            <v-flex 
              data-aos="fade-right"
              data-aos-duration="2000"
              data-aos-mirror="true"
              data-aos-once="false">
              <v-layout
                column
                fill-height
                align-center
                justify-center>
                <div>
                  <v-flex x-12>
                    <span class="display-2">Software Developer, Creative Thinker, Learner.🤓</span>
                  </v-flex>
                  <v-flex 
                    x-12
                    mt-5>
                    <span class="title primary-color font-weight-regular">I'm a web and systems developer, and a computer games enthusiast.</span>
                  </v-flex>
                </div>
              </v-layout>
            </v-flex>
            <v-flex 
              my-5
              data-aos="fade-left"
              data-aos-duration="2000"
              data-aos-mirror="true"
              data-aos-once="false">
              <v-layout
                column
                fill-height
                align-center
                justify-center>
                <div>
                  <v-img
                    src="/undraw_code_review.png"
                    contain
                    height="50vh"
                    width="50vh"
                  ></v-img>
                </div>
              </v-layout>
            </v-flex>
          </v-layout>
        </v-flex>
        <v-flex 
          xs12
          pb-5
          mb-5
          data-aos="fade-up"
          data-aos-duration="2000"
          data-aos-once="false">
          <v-img
            src="/about_me.jpg"
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
  mounted() {
    AOS.init();
  },
}
</script>
