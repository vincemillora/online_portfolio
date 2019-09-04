<template>
  <v-layout wrap>
    <v-flex class="web-component">
      <v-layout 
        wrap
        justify-center
        text-xs-center
        text-sm-left>
        <v-flex 
          xs12
          py-5
          data-aos="flip-up"
          data-aos-duration="2000"
          data-aos-once="false">
          <span 
            v-bind:class="{
              'display-3': !$vuetify.breakpoint.xs,
              'display-2 primary-color': $vuetify.breakpoint.xs,
            }">
            <font-awesome-icon :icon="['fas', 'code']"/>
            <br v-if="$vuetify.breakpoint.xs" />
            {{ $t("about_project") }} 
          </span>
        </v-flex>
        <v-flex
          xs12
          pt-5
          :px-5="!$vuetify.breakpoint.xs && !$vuetify.breakpoint.sm"
          v-for="item in projects"
          :key="item.id"
          data-aos="zoom-in"
          data-aos-duration="2000"
          data-aos-once="false"
          data-aos-anchor-placement="bottom">
          <v-hover v-slot:default="{ hover }">
            <v-expand-transition>
              <v-card
                flat
                :dark="hover"
                >
                <v-layout 
                  wrap 
                  align-center
                  justify-center
                  v-bind:class="{
                    'card-right-border-primary-color': projects.indexOf(item) % 2 !== 0 && !$vuetify.breakpoint.xs && !$vuetify.breakpoint.sm,
                    'card-left-border-primary-color': projects.indexOf(item) % 2 === 0 && !$vuetify.breakpoint.xs  && !$vuetify.breakpoint.sm,
                    'card-bottom-border-primary-color': $vuetify.breakpoint.xs  || $vuetify.breakpoint.sm,
                  }">
                  <v-flex
                    xs12 
                    md5
                    text-xs-center
                    v-if="projects.indexOf(item) % 2 === 0 && !$vuetify.breakpoint.xs  && !$vuetify.breakpoint.sm">
                    <span class="title font-weight-bold">Still Under Development</span> <br/><br/>
                    <span class="title">I will post my projects here as soon as I can. </span> <br/><br/> 
                  </v-flex>
                  <v-flex 
                    xs12
                    md7>
                    <v-img
                      :aspect-ratio="16/9"
                      src="/undraw_under_construction.png">
                        <div
                          v-if="hover"
                          class="d-flex black reveal"
                          style="height: 100%;">
                        </div>
                    </v-img>
                  </v-flex>
                  <v-flex
                    xs12 
                    md5
                    text-xs-center
                    v-if="projects.indexOf(item) % 2 !== 0 || $vuetify.breakpoint.xs || $vuetify.breakpoint.sm">
                    <span class="title font-weight-bold">Still Under Development</span> <br/><br/>
                    <span class="title">I will post my projects here as soon as I can. </span> <br/><br/>
                    <!-- <span class="subtitle-1">asdad</span>   -->
                  </v-flex>
                </v-layout>
              </v-card>
            </v-expand-transition>
          </v-hover>
        </v-flex>
      </v-layout>
    </v-flex>
  </v-layout>
</template>

<script>
import AOS from 'aos';
import 'aos/dist/aos.css';

export default {
  data() {
    return {
      projects: [
        {
          id: 1,
          company: '株式会社Jellyfish',
          position: 'Junior Front-end Web Developer',
          location: 'Tokyo, Japan 🇯🇵',
          link: 'https://jellyfish-g.co.jp/en/',
        },
        {
          id: 2,
          company: '株式会社Tart',
          position: 'Blockchain Developer',
          location: 'Tokyo, Japan 🇯🇵',
          link: 'https://www.tart.tokyo/',
        },
      ],
    }
  },
  mounted() {
    AOS.init();
  },
}
</script>
