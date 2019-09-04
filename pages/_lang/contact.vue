<template>
  <v-layout 
    wrap
    class="web-component">
    <v-flex
      xs12 
      pt-5 
      text-xs-center>
      <v-layout 
        wrap
        fill-height
        align-center>
        <v-flex 
          xs12
          md6
          my-5
          text-xs-center
          text-md-left
          data-aos="flip-left"
          data-aos-duration="1000"
          data-aos-once="false">
          <v-flex xs12>
            <span 
              v-bind:class="{
                'display-2': !$vuetify.breakpoint.xs,
                'display-1': $vuetify.breakpoint.xs,
              }">
              {{ $t('contact_page.contact_intro') }}🙂
            </span>
          </v-flex>
          <v-flex 
            xs12
            mt-3
            mb-5>
            <span class="title primary-color font-weight-regular"> {{ $t('contact_page.contact_details') }} </span>
          </v-flex>
          <v-flex xs12>                
            <v-layout 
              wrap 
              mb-4>
              <v-flex 
                xs12
                md8>
                <span class="title">{{address}}</span>
              </v-flex>
              <v-flex 
                xs12
                md4
                text-md-right
                text-xs-center>
                <span class="title font-weight-bold">
                  {{ $t('contact_page.address_name') }}
                  <font-awesome-icon 
                    color="#41B883" 
                    :icon="['fas', 'map-marker-alt']"/>
                </span>
              </v-flex>
            </v-layout>
            <v-layout 
              wrap
              mb-4>
              <v-flex 
                xs12
                md8>
                <span class="title">
                    {{call}}(
                    <font-awesome-icon 
                      color="#41B883" 
                      :icon="['fas', 'phone-volume']"/>
                    ) <br/> {{text}}(
                    <font-awesome-icon 
                      color="#41B883" 
                      :icon="['fas', 'sms']"/>
                    )
                </span>
              </v-flex>
              <v-flex 
                xs12
                md4
                text-md-right
                text-xs-center>
                <span class="title font-weight-bold">
                  {{ $t('contact_page.contactNumber_name') }}
                  <font-awesome-icon 
                    color="#41B883" 
                    :icon="['fas', 'mobile']"/>
                </span>
              </v-flex>
            </v-layout>
            <v-layout 
              wrap
              mb-4>
              <v-flex 
                xs12
                md8>
                <span class="title">
                  {{line}}
                </span>
              </v-flex>
              <v-flex 
                xs12
                md4
                text-md-right
                text-xs-center>
                <span class="title font-weight-bold">
                  {{ $t('contact_page.line_name') }}
                  <font-awesome-icon 
                    color="#41B883" 
                    :icon="['fab', 'line']"/>
                </span>
              </v-flex>
            </v-layout>
            <v-layout 
              wrap
              mb-4>
              <v-flex 
                xs12
                md8>
                <a 
                  class="title"
                  @click="sendMail()">
                  {{email}}
                </a>
              </v-flex>
              <v-flex 
                xs12
                md4
                text-md-right
                text-xs-center>
                <span class="title font-weight-bold">
                  {{ $t('contact_page.email_name') }}
                  <font-awesome-icon 
                    color="#41B883" 
                    :icon="['fas', 'envelope-open-text']"/>
                </span>
              </v-flex>
            </v-layout>
          </v-flex>
        </v-flex>
        <v-flex
          xs12
          md6
          data-aos="flip-right"
          data-aos-duration="1000"
          data-aos-once="false"
          data-aos-anchor-placement="bottom">
          <v-img
            src="/undraw_contact_us.png"
            contain
            v-bind:width="{
              '70vh': !$vuetify.breakpoint.xs && !$vuetify.breakpoint.sm,
              '100%': $vuetify.breakpoint.xs || $vuetify.breakpoint.sm,
            }"
          ></v-img>
        </v-flex>
      </v-layout>
    </v-flex>
    <v-flex 
      xs12
      px-3
      text-xs-center
      data-aos="flip-up"
      data-aos-duration="1000"
      data-aos-once="false">
      <span class="subheading"> 
        {{ $t('contact_page.resume') }} <br/>
        <font-awesome-icon 
          color="#41B883" 
          :icon="['fas', 'long-arrow-alt-down']"/> <br/>
        <v-flex text-xs-center>
          <v-btn 
            depressed
            class="social-button-wrapper"
            @click="openLink('https://drive.google.com/file/d/11HGKUDt-yN5KZV4Umf-xhnDcUph5YnjK/view?usp=sharing')"
            target="_blank">
            <span 
              class="title"
              id="icon">
              English
            </span>
          </v-btn>
          <v-btn 
            depressed
            class="social-button-wrapper"
            @click="openLink('https://drive.google.com/file/d/14tBU9NPkO_-btrQgulE_1FEbZoUMx5Fz/view?usp=sharing')"
            target="_blank">
            <span 
              class="title"
              id="icon">
              履歴書
            </span>
          </v-btn>
          <v-btn 
            depressed
            class="social-button-wrapper"
            @click="openLink('https://drive.google.com/file/d/16CaA2VC18B_dYe0Pac99KdQjFE3et8SX/view?usp=sharing')"
            target="_blank">
            <span 
              class="title"
              id="icon">
              職務経歴書
            </span>
          </v-btn>
        </v-flex>
      </span>
    </v-flex>
    <v-flex 
      xs12
      mt-3
      mb-5 
      text-xs-center
      data-aos="flip-up"
      data-aos-duration="1000"
      data-aos-once="false">
      <span>
        {{ $t('contact_page.social_accounts') }} <br/>
        <font-awesome-icon 
          color="#41B883" 
          :icon="['fas', 'long-arrow-alt-down']"/> <br/>
      </span>
      <v-btn 
        fab
        depressed
        class="social-button-wrapper"
        href="https://www.facebook.com/vince.millora"
        target="_blank">
        <span 
          class="title"
          id="icon">
          <font-awesome-icon  
            :icon="['fab', 'facebook-f']"/>
        </span>
      </v-btn>
      <v-btn 
        fab
        depressed
        class="social-button-wrapper"
        href="https://twitter.com/VinceMillora"
        target="_blank">
        <span 
          class="title"
          id="icon">
          <font-awesome-icon  
            :icon="['fab', 'twitter']"/>
        </span>
      </v-btn>
      <v-btn 
        fab
        depressed
        class="social-button-wrapper"
        href="https://www.instagram.com/vcmillora/"
        target="_blank">
        <span 
          class="title"
          id="icon">
          <font-awesome-icon  
            :icon="['fab', 'instagram']"/>
        </span>
      </v-btn>
      <v-btn 
        fab
        depressed
        class="social-button-wrapper"
        href="https://www.linkedin.com/in/vince-millora-3606a0143/"
        target="_blank">
        <span 
          class="title"
          id="icon">
          <font-awesome-icon  
            :icon="['fab', 'linkedin-in']"/>
        </span>
      </v-btn>
      <v-btn 
        fab
        depressed
        class="social-button-wrapper"
        href="https://github.com/vincemillora"
        target="_blank">
        <span 
          class="title"
          id="icon">
          <font-awesome-icon  
            :icon="['fab', 'github']"/>
        </span>
      </v-btn>
      <v-btn 
        fab
        depressed
        class="social-button-wrapper"
        href="https://qiita.com/Binsu"
        target="_blank">
        <span 
          class="title"
          id="icon">
          <font-awesome-icon  
            :icon="['fas', 'newspaper']"/>
        </span>
      </v-btn>
    </v-flex>
  </v-layout>
</template>

<script>
import AOS from 'aos';
import 'aos/dist/aos.css';

export default {
  data() {
    return {
      address: 'Kawai 594, Okutama City, Nishitama District, Tokyo, Japan 🇯🇵',
      email: 'vcmillora@up.edu.ph',
      call: '050-6868-9176',
      text: '080-7695-7291',
      line: 'vcmillora',
    }
  },
  mounted() {
    AOS.init();
  },
  methods: {
    sendMail(){
      window.open('mailto:'+this.email);
    },
    openLink(link){
      window.open(link);
    },
  }
}
</script>
