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
          :pa-5="!$vuetify.breakpoint.xs && !$vuetify.breakpoint.sm"
          data-aos="fade-up"
          data-aos-duration="2000"
          data-aos-once="false">
          <v-hover v-slot:default="{ hover }">
            <v-expand-transition>
              <v-card
                flat
                :dark="hover">
                <v-layout wrap>
                <v-flex md6>
                  <v-img
                    :aspect-ratio="16/9"
                    src="https://cdn.vuetifyjs.com/images/cards/kitchen.png">
                      <div
                        v-if="hover"
                        class="d-flex black reveal"
                        style="height: 100%;">
                      </div>
                  </v-img>
                </v-flex>
                <v-flex 
                  md6
                  class="card-right-border-primary-color">
                    <div class="font-weight-light title mb-2">For the perfect meal</div>
                    <h3 class="display-1 font-weight-light mb-2">QW cooking utensils</h3>
                    <div class="font-weight-light title mb-2">
                      Our Vintage kitchen utensils delight any chef.<br>
                      Made of bamboo by hand
                    </div>
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
  mounted() {
    AOS.init();
  },
}
</script>
