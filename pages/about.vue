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
          pl-1
          py-5
          data-aos="flip-up"
          data-aos-duration="1000"
          data-aos-once="false">
          <span 
            v-bind:class="{
              'display-3': !$vuetify.breakpoint.xs,
              'display-2 primary-color': $vuetify.breakpoint.xs,
            }">
            <font-awesome-icon :icon="['fas', 'user-tie']"/>
            <br v-if="$vuetify.breakpoint.xs" />
            Who am I
          </span>
        </v-flex>
        <v-flex>
          <v-layout 
            wrap
            fill-height
            align-center>
            <v-flex 
              xs12
              sm8
              :pa-5="!$vuetify.breakpoint.xs"
              data-aos="fade-up-right"
              data-aos-duration="1000"
              data-aos-once="false"
              data-aos-anchor-placement="bottom">
              <span class="title"> {{ about }} </span>
              <span class="title"> Right now, I'm looking for a job opportunity and I hope I could interest you in some way or another. You can checkout my resume <a @click="openLink('https://drive.google.com/file/d/1qIuwWvRrsr-SkA2S0QGQzq2Rv7QSNLfl/view?usp=sharing')">here</a> just in case.</span> 
            </v-flex>
            <v-flex 
              v-if="!$vuetify.breakpoint.xs"
              sm4 
              data-aos="fade-up-left"
              data-aos-duration="1000"
              data-aos-once="false"
              data-aos-anchor-placement="bottom">
              <v-img
                class="profile-pic"
                src="/prof_pic.jpg"
                contain
                width="400px"
              ></v-img>
            </v-flex>
          </v-layout>
        </v-flex>
      </v-layout>
      <v-layout
        wrap
        text-xs-center
        text-sm-left>
        <v-flex 
          xs12
          py-5
          data-aos="flip-up"
          data-aos-duration="1000"
          data-aos-once="false">
          <span 
            v-bind:class="{
              'display-3': !$vuetify.breakpoint.xs,
              'display-2 primary-color': $vuetify.breakpoint.xs,
            }"> 
            <font-awesome-icon :icon="['fas', 'brain']"/>
            <br v-if="$vuetify.breakpoint.xs" />
            What I Know
          </span>
        </v-flex>
        <v-flex 
          xs12
          :pa-5="!$vuetify.breakpoint.xs">
          <v-layout wrap>
            <v-flex 
              xs12
              sm6
              :pl-5="!$vuetify.breakpoint.xs">
              <v-flex
                data-aos="flip-up"
                data-aos-duration="1000"
                data-aos-once="false">
                <span class="headline font-weight-bold primary-color">My Education and Certificates</span>
              </v-flex>
              <v-layout column>
                <v-flex 
                  my-4
                  pt-1
                  pl-3
                  v-for="item in education"
                  :key="item.id"
                  text-xs-left
                  class="card-left-border-primary-color"
                  data-aos="fade-up-right"
                  data-aos-duration="1000"
                  data-aos-once="false"
                  data-aos-anchor-placement="bottom">
                  <span class="title"> {{item.type}} </span>
                  <v-flex 
                    xs12
                    sm9
                    md8
                    pt-3
                    text-xs-right>
                    <span class="title primary-color"> {{item.degree}} </span> <br/>
                    <span> {{item.focus}} </span> <br/>
                    <span> {{item.time}} </span> <br/>
                  </v-flex>
                </v-flex>
              </v-layout>
            </v-flex>
            <v-flex 
              xs12
              sm6
              :pl-5="!$vuetify.breakpoint.xs">
              <v-flex
                data-aos="flip-up"
                data-aos-duration="1000"
                data-aos-once="false">
                <span class="headline font-weight-bold primary-color">My Skills</span>
              </v-flex>
              <v-layout 
                column
                text-xs-left>
                <v-flex 
                  my-4
                  pt-1
                  v-for="item in skills"
                  :key="item.id"
                  data-aos="fade-up-left"
                  data-aos-duration="1000"
                  data-aos-once="false"
                  data-aos-anchor-placement="bottom">
                  <span class="title primary-color"> {{item.title}} </span>
                  <v-flex 
                    mt-3
                    ml-3
                    pl-3
                    class="card-left-border-secondary-color"
                    v-for="skill in item.items"
                    :key="skill.name">
                    <span class="title"> {{skill.name}} <br/></span>
                  </v-flex>
                </v-flex>
              </v-layout>
            </v-flex>
          </v-layout>
        </v-flex>
      </v-layout>
      <v-layout column>
        <v-flex
          xs12 
          pl-1
          py-5
          text-xs-center
          text-sm-left
          data-aos="flip-up"
          data-aos-duration="1000"
          data-aos-once="false"
          data-aos-anchor-placement="bottom">
          <span 
            v-bind:class="{
              'display-3': !$vuetify.breakpoint.xs,
              'display-2 primary-color': $vuetify.breakpoint.xs,
            }">
            <font-awesome-icon :icon="['fas', 'road']"/>
            <br v-if="$vuetify.breakpoint.xs" />
            Where I've been
          </span>
        </v-flex>
        <v-flex>
          <v-layout
            wrap  
            :pa-5="!$vuetify.breakpoint.xs"           
            justify-center>
            <v-flex
              xs12
              md10
              class="timeline"
              v-for="item in experience"
              :key="item.id"
              data-aos="fade-right"
              data-aos-duration="1000"
              data-aos-once="false"
              data-aos-anchor-placement="bottom">
              <v-layout 
                row 
                wrap
                :justify-end="experience.indexOf(item) % 2 !== 0">
                <v-flex 
                  xs12
                  md1
                  v-if="experience.indexOf(item) % 2 !== 0 || $vuetify.breakpoint.xs">
                  <span 
                    class="headline font-weight-bold white--text"><span class="timeline-number">{{item.id}}</span>
                  </span>
                </v-flex>
                <v-flex 
                  xs12
                  md11
                  :pt-4="$vuetify.breakpoint.xs">
                  <span class="title font-weight-bold">{{item.company}}</span> as a 
                  <span class="title primary-color">{{item.position}}</span> <br/>
                  <span>{{item.time}}</span><br/>
                  <span>{{item.location}}</span> 
                </v-flex>
                <v-flex 
                  md1
                  v-if="experience.indexOf(item) % 2 === 0 && !$vuetify.breakpoint.xs">
                  <span
                    class="headline font-weight-bold white--text"><span class="timeline-number">{{item.id}}</span>
                  </span>
                </v-flex>
                <v-flex 
                  xs12
                  md11>
                  <v-flex mt-3>
                    <span v-bind:class="{
                      'title': !$vuetify.breakpoint.xs,
                    }"> 
                      {{item.body}} 
                    </span>
                  </v-flex>
                  <v-flex mt-2>
                    <span > You can find out more about the company <a @click="openLink(item.link)">here</a>. </span>
                  </v-flex>
                </v-flex>
              </v-layout>
            </v-flex>
          </v-layout>
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
      about: "Hi there, my name is Vince Millora, a guy from the Philippines 🇵🇭🇵🇭. I'm a developer —a software developer— that enjoys coding " + 
      "and solving different logical problems. I'm currently a student studying the Japanese language at " +
      "Bridge Institute of Technology in Okutama, Tokyo, Japan. I'm residing in the dormitory of the school. " + 
      "In the morning, I study the Japanese language by developing an I.T. project " +
      "and during the end of the school's semester, I present my project using Japanese. In the afternoon, " + 
      "I'm a Web Developer of 株式会社Jellyfish.",
      experience: [
        {
          id: 1,
          company: '株式会社Jellyfish',
          position: 'Junior Front-end Web Developer',
          location: 'Tokyo, Japan 🇯🇵',
          time: "April 2019 - Present",
          body: '株式会社Jellyfish is a company that helps people around the ' + 
                'world to find opportunities in Japan. I too was someone who ' + 
                'took an opportunity from 株式会社Jellyfish and became a Japanese ' + 
                'language student and a Web Developer at Bridge Institute of Technology ' + 
                '(BIT). Specifically, I am a member of the front-end development team of ' + 
                "BIT's I.T. division.",
          link: 'https://jellyfish-g.co.jp/en/',
        },
        {
          id: 2,
          company: '株式会社Jellyfish',
          position: 'Blockchain Developer',
          location: 'Tokyo, Japan 🇯🇵',
          time: "October 2018 - March 2019",
          body: 'Before I became a Front-end Web Developer at 株式会社Jellyfish, ' + 
                'I participated in a Blockchain bootcamp at Bridge Institute of Technology ' + 
                'for 3 months. After the bootcamp, I was recruited as a Blockchain Developer ' + 
                'for one of the projects  of the company. I was a member of that project ' + 
                'until the project closed March of 2019. ',
          link: 'http://bit-okutama.jp/',
        },
        {
          id: 3,
          company: 'Next BPO Solutions, Inc.',
          position: 'Web Developer',
          location: 'Davao City, Philippines 🇵🇭',
          time: "August 2017 - August 2018",
          body: 'My first full-time job was at Next BPO Solutions, Inc. as a Web Developer. ' + 
                'Next BPO Solutions is an outsourcing company and I was assigned to a project from  ' + 
                'DXC Technology, a company that resulted from the merger of Hewlett Packard Enterprise ' + 
                'and Computer Sciences Corporation. I was with the project until I left for Japan. ',
          link: 'https://www.nextbposolutions.com/',
        },
        {
          id: 4,
          company: 'University of the Philippines Mindanao LiDAR II Project',
          position: 'Project Intern',
          location: 'Davao City, Philippines 🇵🇭',
          time: "June 2016 - July 2016",
          body: 'University of the Philippines requires its students to do an internship that is based ' +
                "on the student's focus of study. Since I was focusing on Computer Sciences, I was assigned " +
                "to the I.T. department of my university's  LiDAR II Project. This was my first experience in a " + 
                'working environment and with a team of developers. Also, it was my first time using Git and I ' + 
                'learned the importance of source control.',
          link: 'https://www.glunis.com/PH/Davao-City/1587352928186470/UP-Mindanao-Phil-Lidar-2',
        },
      ],
      education: [
        {
          id: 1,
          type: "Bridge Institute of Technology",
          degree: "Certificate of Completion",
          focus: "Japanese Language",
          time: "2018 - 2020",
        },
        {
          id: 2,
          type: "PhilNITS (J.I.T.S.E.)",
          degree: "I.T. Passport Certification",
          focus: "Certificate",
          time: "2018",
        },
        {
          id: 3,
          type: "University of the Philippines",
          degree: "Bachelor's Degree",
          focus: "Computer Science",
          time: "2013 - 2017",
        },
      ],
      skills: [
        {
          title: 'Programming',
          items: [
            {
              name: 'Front-end Web Development (SASS, Vue, React)',
            },
            {
              name: 'Software Development (Java, C#)',
            },
            {
              name: 'Mobile Development (Java, React Native)',
            },
            {
              name: 'Database Design',
            },
            {
              name: 'Database Programming (MySQL, SQLite)',
            },
            {
              name: 'Blockchain Development (Ethereum)',
            },
          ],
        },
        {
          title: 'Design',
          items: [
            {
              name: 'Adobe Photoshop',
            },
            {
              name: 'Adobe Illustrator',
            },
            {
              name: 'UI Design',
            },
            {
              name: 'Wireframe Design',
            },
            {
              name: 'Graphic Design',
            },
          ],
        },
        {
          title: 'Language',
          items: [
            {
              name: 'Filipino (Native)',
            },
            {
              name: 'English (Bilingual)',
            },
            {
              name: 'Japanese (Conversational)',
            },
          ],
        },
      ],
    }
  },
  mounted() {
    AOS.init();
  },
  methods: {
    openLink(link) {
      window.open(link);
    }
  }
}
</script>
