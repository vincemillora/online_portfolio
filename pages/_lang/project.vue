<template>
  <v-layout wrap>
    <v-flex class="web-component">
      <v-layout 
        wrap
        justify-center
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
          pt-3
          :px-2="!$vuetify.breakpoint.xs && !$vuetify.breakpoint.sm"
          v-for="item in projects"
          :key="item.id"
          :md6="item.type === 'desktop'"
          :md4="item.type === 'mobile'"
          data-aos="zoom-in"
          data-aos-duration="2000"
          data-aos-once="false"
          data-aos-anchor-placement="bottom">
          <v-hover v-slot:default="{ hover }">
            <v-expand-transition>
              <v-card 
                height="350px" 
                class="cursor-pointer"
                @click="showDetails()">
                <div class="back-image">
                  <v-img
                    height="100%"
                    width="100%"
                    :src="item.imgSrc">
                      <div
                        v-if="hover"
                        class="d-flex black reveal"
                        style="height: 100%;">
                      </div>
                  </v-img>
                </div>
                <div class="front-description">
                  <v-flex 
                    ma-3 
                    v-bind:class="{
                      'white--text': hover
                    }">
                    <span class="title font-weight-bold">{{item.title}}</span> <br/>
                    <span class="body">{{item.subtitle}}</span>
                  </v-flex>
                </div>
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
          type: 'mobile',
          title: 'Yonmoque',
          subtitle: 'Mobile Game',
          imgSrc: '/projects/Yonmoque.jpg',
          link: 'https://jellyfish-g.co.jp/en/',
        },
        {
          id: 2,
          type: 'desktop',
          title: 'Babel Method',
          subtitle: 'E-learning Plarform',
          imgSrc: '/projects/Babel-method.png',
          link: 'https://www.tart.tokyo/',
        },
        {
          id: 3,
          type: 'desktop',
          title: 'CryptoViper',
          subtitle: 'E-learning Plarform',
          imgSrc: '/projects/Cryptoviper.jpg',
          link: 'https://www.tart.tokyo/',
        },
      ],
    }
  },
  mounted() {
    AOS.init();
  },
  methods: {
    showDetails() {
      alert('This feature will come soon.')
    }
  }
}
</script>
