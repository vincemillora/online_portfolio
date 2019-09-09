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
            {{ $t("about_page.aboutMe_title") }} 
          </span>
        </v-flex>
        <v-flex>
          <v-layout 
            wrap
            fill-height
            align-center>
            <v-flex 
              xs12
              sm12
              :pa-5="!$vuetify.breakpoint.xs && !$vuetify.breakpoint.sm"
              data-aos="zoom-in"
              data-aos-duration="1000"
              data-aos-once="false"
              data-aos-anchor-placement="bottom">
              <span class="title" v-if="$i18n.locale === 'en'"> 
                Hi there, my name is Vince Carreon Millora, a guy from the Philippines 🇵🇭🇵🇭. I am a software developer that enjoys coding
                and solving complex problems. I have experiences in using different technologies; I've been a back-end developer designing databases and APIs, a Blockchain developer 
                creating Smart Contracts, and a front-end engineer designing and creating web and mobile systems. In every position I've been, and every tasks I had, I've always aimed
                for a good result that would not only satisfy myself, but also the team and the client. I'm a teamplayer that is always ready to assist my teammates when they are in need. 
                That's why one of my goal as a developer is to become a Full-Stack, so that I will be able to produce good results and assist my team even if the task is back-end or front-end. <br/><br/>
                
                Currently, I am studying the Japanese language at <a @click="openLink('http://bit-okutama.jp/')">Bridge Institute of Technology</a> to efficiently deliver my thoughts and solutions even while staying in Japan. 
                In the morning, I study Japanese by developing an I.T. project and during the end of the school's semester, I present my project using Japanese. In the afternoon, 
                I am a Web Developer of <a @click="openLink('https://jellyfish-g.co.jp/en/')">株式会社JELLYFISH</a>. <br/><br/>
                
                As a junior developer, I'm always open for new opportunities that will enhance my current skills. I hope I could interest you in some way or another. 
                You can checkout my resume here just in case.
              </span> 
              <span class="title" v-else>
                こんにちは！ビンス・カリヨン・ミルヨラです。フィリピンから参りました。私は、コーディングの複雑な問題の解決を楽しんでいるソフトウェア開発者です。私は、バックエンド開発者としてデータベースとAPIを設計したり、ブロックチェーン開発者としてスマートコントラクトを作成したり、
                およびフロントエンド開発者としてWebとモバイルのUIを設計して作成したりした経験があります。今までに働いていたすべてのポジションとタスクにおいて、自分自身だけではなくチームとクライアントも満足させる良い結果を常に目指してきました。私はチームメイトが助けが必要なときに、
                いつでもチームメイトを手伝えるチームプレーヤーです。開発者として、私の1つの目標がフルスタックになることです。そのため、タスクがバックエンドでもフロントエンドでも、私は良い結果を出したり、チームを手伝ったりすることができます。<br/><br/>

                現在私は日本の<a @click="openLink('http://bit-okutama.jp/')">Bridge Institute of Technology</a>で日本語を勉強しています。午前中に、ITのプロジェクトを開発しながら、日本語を勉強しています。学期末前に、私は日本語で奥多摩人々にプロジェクトを発表します。
                午後は、<a @click="openLink('https://jellyfish-g.co.jp/en/')">株式会社JELLYFISH</a>のウェブ開発者しています。<br/><br/>

                開発者として、スキルを改善するために、私はエンジニア機会を挑戦したいです。あなたに興味を持っていただければ幸いです。ここで私の履歴書と職務経歴書をチェックできます。よろしくお願いします。
              </span>
              <v-flex 
                mt-3
                text-sm-right>
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
            </v-flex>
            
            <!-- <v-flex 
              v-if="!$vuetify.breakpoint.xs && !$vuetify.breakpoint.sm"
              md4
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
            </v-flex> -->
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
            {{ $t("about_page.knowledge_title") }} 
          </span>
        </v-flex>
        <v-flex 
          xs12
          :pa-5="!$vuetify.breakpoint.xs && !$vuetify.breakpoint.sm">
          <v-layout wrap>
            <v-flex 
              xs12
              sm6
              :pl-5="!$vuetify.breakpoint.xs && !$vuetify.breakpoint.sm">
              <v-flex
                data-aos="flip-up"
                data-aos-duration="1000"
                data-aos-once="false">
                <span class="headline font-weight-bold primary-color">{{ $t("about_page.education_name") }} </span>
              </v-flex>
              <v-layout column>
                <v-flex 
                  my-4
                  pt-1
                  pl-3
                  v-for='item in $t("education")'
                  :key="item.id"
                  text-xs-left
                  class="card-left-border-primary-color"
                  data-aos="fade-right"
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
              :pl-5="!$vuetify.breakpoint.xs && !$vuetify.breakpoint.sm">
              <v-flex
                data-aos="flip-up"
                data-aos-duration="1000"
                data-aos-once="false">
                <span class="headline font-weight-bold primary-color">{{ $t("about_page.skill_name") }} </span>
              </v-flex>
              <v-layout 
                column
                text-xs-left>
                <v-flex 
                  my-4
                  pt-1
                  v-for='item in $t("skills")'
                  :key="item.id"
                  :data-aos="animation"
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
      
    </v-flex>
    <v-flex class="web-component tertiary-color-background">
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
            {{ $t("about_page.experience_title") }} 
          </span>
        </v-flex>
        <v-layout
          wrap  
          :pa-5="!$vuetify.breakpoint.xs && !$vuetify.breakpoint.sm"           
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
                v-if="experience.indexOf(item) % 2 !== 0 || $vuetify.breakpoint.xs || $vuetify.breakpoint.sm">
                <span 
                  class="headline font-weight-bold white--text"><span class="timeline-number">{{item.id}}</span>
                </span>
              </v-flex>
              <v-flex 
                xs12
                md11
                :pt-4="$vuetify.breakpoint.xs || $vuetify.breakpoint.sm">
                <span class="title font-weight-bold">{{item.company}}</span> {{$t('about_page.as_a')}}
                <span class="title primary-color">{{item.position}}</span> <br/>
                <span>{{item.time}}</span><br/>
                <span>{{item.location}}</span> 
              </v-flex>
              <v-flex 
                md1
                v-if="experience.indexOf(item) % 2 === 0 && !$vuetify.breakpoint.xs  && !$vuetify.breakpoint.sm">
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
      </v-layout>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  data() {
    return {
      animation:'fade-left',
      experience: [
        {
          id: 1,
          company: '株式会社Jellyfish',
          position: 'Junior Front-end Web Developer',
          location: 'Tokyo, Japan 🇯🇵',
          time: "April 2019 - Present",
          body: '株式会社Jellyfish is a company that assists people around the ' + 
                'world to find opportunities in Japan. I was someone who ' + 
                'took an opportunity from 株式会社Jellyfish and became a Japanese ' + 
                'language student at Bridge Institute of Technology (BIT) while doing ' + 
                'a part-time job as a developer at 株式会社Jellyfish. Specifically, ' + 
                "I am a member of the front-end development team of BIT's I.T. division.",
          link: 'https://jellyfish-g.co.jp/en/',
        },
        {
          id: 2,
          company: '株式会社Tart',
          position: 'Blockchain Developer',
          location: 'Tokyo, Japan 🇯🇵',
          time: "October 2018 - March 2019",
          body: 'Before I became a Front-end Web Developer at 株式会社Jellyfish, ' + 
                'I participated in a Blockchain bootcamp at Bridge Institute of Technology ' + 
                'for 3 months. After the bootcamp, I was recruited as a Blockchain Developer by 株式会社Tart ' + 
                'for one of the projects  of 株式会社Jellyfish. I was a member of that project ' + 
                'until 株式会社Tart parted ways with 株式会社Jellyfish on March of 2019. ',
          link: 'https://www.tart.tokyo/',
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
    this.onResize();
    window.addEventListener('resize', this.onResize, { passive: true });
  },
  methods: {
    openLink(link) {
      window.open(link);
    },
    onResize() {
      if(window.innerWidth < 960) {
        this.animation = 'fade-right';
      } else {
        this.animation = 'fade-left';
      }
    },
  }
}
</script>
