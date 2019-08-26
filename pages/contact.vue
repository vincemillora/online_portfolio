<template>
  <v-layout wrap>
    <v-flex pt-5 text-xs-center class="web-component">
      <v-layout>
        <v-flex my-5>
          <v-layout
            column
            fill-height
            align-center
            justify-center
            text-xs-right>
            <div>
              <v-flex xs12>
                <span class="display-2">Say hello, feel free to drop a message.🙂</span>
              </v-flex>
              <v-flex 
                xs12
                mt-3
                mb-5>
                <span class="title primary-color font-weight-regular">Here are my contact details: </span>
              </v-flex>
              <v-flex xs12>                
                <v-layout mb-4>
                  <v-flex xs8>
                    <span class="title">{{address}}</span>
                  </v-flex>
                  <v-flex 
                    xs4
                    text-xs-right>
                    <span class="title font-weight-bold">
                      Address
                      <font-awesome-icon 
                        color="#41B883" 
                        :icon="['fas', 'map-marker-alt']"/>
                    </span>
                  </v-flex>
                </v-layout>
                <v-layout mb-4>
                  <v-flex xs8>
                    <span class="title">
                        {{call}}(
                        <font-awesome-icon 
                          color="#41B883" 
                          :icon="['fas', 'phone-volume']"/>
                        ) | {{text}}(
                        <font-awesome-icon 
                          color="#41B883" 
                          :icon="['fas', 'sms']"/>
                        )
                    </span>
                  </v-flex>
                  <v-flex 
                    xs4
                    text-xs-right>
                    <span class="title font-weight-bold">
                      Contact Number
                      <font-awesome-icon 
                        color="#41B883" 
                        :icon="['fas', 'mobile']"/>
                    </span>
                  </v-flex>
                </v-layout>
                <v-layout mb-4>
                  <v-flex xs8>
                    <span class="title">
                      {{line}}
                    </span>
                  </v-flex>
                  <v-flex 
                    xs4
                    text-xs-right>
                    <span class="title font-weight-bold">
                      Line
                      <font-awesome-icon 
                        color="#41B883" 
                        :icon="['fab', 'line']"/>
                    </span>
                  </v-flex>
                </v-layout>
                <v-layout mb-4>
                  <v-flex xs8>
                    <a 
                      class="title"
                      @click="sendMail()">
                      {{email}}
                    </a>
                  </v-flex>
                  <v-flex 
                    xs4
                    text-xs-right>
                    <span class="title font-weight-bold">
                      Email
                      <font-awesome-icon 
                        color="#41B883" 
                        :icon="['fas', 'envelope-open-text']"/>
                    </span>
                  </v-flex>
                </v-layout>
              </v-flex>
            </div>
          </v-layout>
        </v-flex>
        <v-flex>
          <v-layout
            column
            fill-height
            align-center
            justify-center>
            <div>
              <v-img
                src="/undraw_contact_us.png"
                contain
                width="70vh"
              ></v-img>
            </div>
          </v-layout>
        </v-flex>
      </v-layout>
    </v-flex>
    <v-flex mb-5 text-xs-center>
      <span class="subheading font-weight-thin">
        Or, you can contact me through my social media accounts here.
        <br/>
        <font-awesome-icon 
          color="#41B883" 
          :icon="['fas', 'long-arrow-alt-down']"/>
      </span>
    </v-flex>
  </v-layout>
</template>

<script>

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
  methods: {
    sendMail(){
      window.open('mailto:'+this.email);
    }
  }
}
</script>
