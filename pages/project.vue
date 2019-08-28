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
            What I've Done
          </span>
        </v-flex>
        <v-flex
          data-aos="fade-up"
          data-aos-duration="2000"
          data-aos-once="false">
          <v-card>
            <v-layout wrap justify-center py-5>
              <v-layout
                column
                fill-height
                align-center
                justify-center>
                <div>
                  <v-flex xs12>
                    <v-img
                      src="/undraw_under_construction.png"
                      contain
                      v-bind:height="{
                        '50vh': !$vuetify.breakpoint.xs,
                      }"
                      width="50vw"
                    ></v-img>
                  </v-flex>
                </div>
              </v-layout>
              <span
                v-bind:class="{
                  'title': !$vuetify.breakpoint.xs,
                }"> 
                This part is still under development. I'm working on it and will post my projects here as soon as I can. 
              </span>
            </v-layout>
          </v-card>
        </v-flex>
      </v-layout>
    </v-flex>
  </v-layout>
</template>

<script>
import AOS from 'aos';
import 'aos/dist/aos.css';

export default {
  mounted() {
    AOS.init();
  },
}
</script>
