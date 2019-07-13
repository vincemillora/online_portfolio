<template>
  <v-layout 
    wrap
    row>
    <v-flex class="web-component">
      <v-layout>
        <v-flex>
          <v-layout
            column
            fill-height
            align-center
            justify-center>
            <div>
              <v-flex x-12>
                <span class="display-2">Software Developer, Creative Thinker, Learner.</span>
              </v-flex>
              <v-flex 
                x-12
                mt-5>
                <span class="title primary-color font-weight-regular">I'm a web and systems developer, and a computer games enthusiast.</span>
              </v-flex>
            </div>
          </v-layout>
        </v-flex>
        <v-flex my-5>
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
    <v-flex xs12>
      <v-img
        src="/about_me.jpg"
        width="100%"
      ></v-img>
    </v-flex>
    <v-flex class="web-component">
      <v-layout mb-4>
        <v-flex 
          xs4
          px-5
          text-xs-right>
          <span class="display-1">
            <font-awesome-icon 
              color="#41B883" 
              :icon="['fas', 'user-tie']"/>
            About Me
          </span>
        </v-flex>
        <v-flex 
          xs8
          pa-2>
          <span class="title">{{about}}</span>
        </v-flex>
      </v-layout>
      <v-layout mb-4>
        <v-flex 
          xs4 
          px-5
          text-xs-right>
          <span class="display-1">
            <font-awesome-icon 
              color="#41B883" 
              :icon="['fas', 'briefcase']"/>
            Experience
          </span>
        </v-flex>
        <v-flex 
          xs8
          pa-2>
          <span class="title">{{about}}</span>
        </v-flex>
      </v-layout>
      <v-layout mb-4>
        <v-flex 
          xs4
          px-5
          text-xs-right>
          <span class="display-1">
            <font-awesome-icon 
              color="#41B883" 
              :icon="['fas', 'book-open']"/>
            Education
          </span>
        </v-flex>
        <v-flex 
          xs8
          pa-2>
          <span class="title">{{about}}</span>
        </v-flex>
      </v-layout>
      <v-layout mb-4>
        <v-flex 
          xs4
          px-5
          text-xs-right>
          <span class="display-1">
            <font-awesome-icon 
              color="#41B883" 
              :icon="['fas', 'certificate']"/>
            Achievements
          </span>
        </v-flex>
        <v-flex 
          xs8
          pa-2>
          <span class="title">{{about}}</span>
        </v-flex>
      </v-layout>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  data() {
    return {
      about: 'about me',

    }
  }
}
</script>
