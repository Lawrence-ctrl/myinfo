<template>
  <q-page>
    <div class="home" ref="home">
      <div class="container">
        <div class="row items-center justify-center">
          <div class="col-sm-12 col-md-6" :class="$q.screen.lt.sm ? 'q-mb-xl': ''">
            <div class="hello bg-primary">Hello I'm</div>
            <div class="name">THUTA YAR MOE</div>
            <div class="profession">Web Developer</div>
            <div class="text-body1 q-mb-sm my-info">
              <q-icon name="mail" size="sm" class="q-mr-md" color="primary"/>
              <label>thutayarmoe97@gmail.com</label>
            </div>
            <div class="text-body1 q-mb-sm my-info">
              <q-icon name="phone" size="sm" class="q-mr-md" color="primary"/>
              <label>+959 972 089 188</label>
            </div>
            <div class="text-body1 q-mb-sm my-info">
              <q-icon name="place" size="sm" class="q-mr-md" color="primary"/>
              <label>No.(25), Bozinyaw 3rd street, 30 Quarter, North Dagon, Yangon.</label>
            </div>
          </div>
          <div class="col-md-6 col-sm-12">
            <div class="profile">
              <q-avatar>
                <img src="mine.jpg" class="profile-image">
              </q-avatar>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="about" ref="about">
      <div class="container">
        <div class="text-h4 text-center text-weight-bolder q-pb-lg">“ About Me ”</div>
        <div class="row items-center justify-center">
          <div class="col-12 col-sm-8">
            <div class="text-body1">
              Hi! I'm Thuta Yar Moe. I'm a Backend Developer.
              I studied Information Technology and graduated with bachelor of engineering (IT) from Technological University (Hmawbi).
              I'm very passionate and dedicated to my work. I enjoy every step of the development process, from discussion and collaboration.
              I have many experiences in website and mobile application development. I am good at
            </div>
            <div class="languages q-py-md">
              <q-chip square class="q-pa-md" size="md" color="primary" text-color="white">Vue.js</q-chip>
              <q-chip square class="q-pa-md" size="md" color="primary" text-color="white">NuxtJS</q-chip>
              <q-chip square class="q-pa-md" size="md" color="primary" text-color="white">Quasar</q-chip>
              <q-chip square class="q-pa-md" size="md" color="primary" text-color="white">Laravel</q-chip>
              <q-chip square class="q-pa-md" size="md" color="primary" text-color="white">PHP</q-chip>
              <q-chip square class="q-pa-md" size="md" color="primary" text-color="white">MySQL</q-chip>
              <q-chip square class="q-pa-md" size="md" color="primary" text-color="white">NGINX</q-chip>
              <q-chip square class="q-pa-md" size="md" color="primary" text-color="white">Digital Ocean</q-chip>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="whatido">
      <div class="container">
        <div class="text-h4 text-center text-weight-bolder q-pb-xl">What I Do</div>
        <div class="row justify-center q-col-gutter-lg">
          <div class="col-12 col-sm-8 col-md-6">
            <q-card class="what-i-do text-center shadow-9">
              <q-card-section>
                <q-avatar size="60px" rounded class="q-mr-sm">
                  <img src="~/assets/website3.png" />
                </q-avatar>
                <div v-if="$q.screen.lt.md">
                  Web Development
                </div>
                <span v-else>Web Development</span>
              </q-card-section>
            </q-card>
          </div>
          <div class="col-12 col-sm-8 col-md-6">
            <q-card class="what-i-do text-center shadow-9">
              <q-card-section>
                <q-avatar size="60px" rounded class="q-mr-sm">
                  <img src="~/assets/app.png" style="object-fit:contain"/>
                </q-avatar>
                <div v-if="$q.screen.lt.md">
                  App Development
                </div>
                <span v-else>App Development</span>
              </q-card-section>
            </q-card>
          </div>
        </div>
      </div>
    </div>

    <div class="projects" ref="projects">
      <div class="container">
        <Projects />
      </div>
    </div>

    <div class="skills">
      <div class="container">
        <div class="row justify-center q-col-gutter-x-lg">
          <div class="col-12 col-sm-8 col-md-5 q-mx-md q-mb-lg">
            <div class="text-h4 text-weight-bolder text-center q-pb-xl">Technical Skills</div>
            <div v-for="tech in technical" :key="tech.id">
              <div class="row">
                <div class="col-6 text-dark text-weight-bold tech-name">
                  {{ tech.name }}
                </div>
                <div class="col-6 text-right tech-value text-medium text-weight-bold">
                  {{ tech.percent * 100 }}%
                </div>
              </div>
              <q-linear-progress size="6px" :value="tech.percent" class="q-mt-sm q-mb-md" />
            </div>
          </div>
          <div class="col-12 col-sm-8 col-md-5 q-mx-md">
            <div class="text-h4 text-weight-bolder text-center q-pb-xl">Professional Skills</div>
            <div v-for="pro in professional" :key="pro.id">
              <div class="row">
                <div class="col-6 text-dark text-weight-bold tech-name">
                  {{ pro.name }}
                </div>
                <div class="col-6 text-right tech-value text-medium text-weight-bold">
                  {{ pro.percent * 100 }}%
                </div>
              </div>
              <q-linear-progress size="6px" :value="pro.percent" class="q-mt-sm q-mb-md" />
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="work-experience">
      <div class="container">
        <div class="row justify-center q-col-gutter-x-lg">
          <div class="col-12 col-sm-8 col-md-6 q-mb-lg">
            <div class="text-h4 text-weight-bolder text-center q-pb-xl">Work Experience</div>

            <q-card class="q-mb-lg q-pa-sm shadow-5">
              <q-card-section>
                <div class="text-h6 text-primary text-weight-bolder">YCDC</div>
                <ul>
                  <li class="text-weight-bold">Junior Web Developer</li>
                  <li class="text-weight-bold">June 2019 - July 2019 (Internship)</li>
                </ul>
              </q-card-section>
            </q-card>

            <q-card class="q-mb-lg q-pa-sm shadow-5">
              <q-card-section>
                <div class="text-h6 text-primary text-weight-bolder">CGM</div>
                <ul>
                  <li class="text-weight-bold">Junior Web Developer</li>
                  <li class="text-weight-bold">Feb 2020 - May 2020 (Quit because of COVID 19)</li>
                </ul>
              </q-card-section>
            </q-card>

            <q-card class="q-mb-lg q-pa-sm shadow-5">
              <q-card-section>
                <div class="text-h6 text-primary text-weight-bolder">Datalink</div>
                 <ul>
                  <li class="text-weight-bold">Web Developer</li>
                  <li class="text-weight-bold">June 2020 - July 2021</li>
                </ul>
              </q-card-section>
            </q-card>

          </div>
          <div class="col-12 col-sm-8 col-md-6">
            <div class="text-h4 text-weight-bolder text-center q-pb-xl">Education</div>

            <q-card class="q-mb-lg q-pa-sm shadow-5">
              <q-card-section>
                <div class="text-h6 text-primary text-weight-bolder">Technological University (HMAWBI)</div>
                <ul>
                  <li class="text-weight-bold">2013 - 2019</li>
                  <li class="text-weight-bold">Bachelor of Technology (IT)</li>
                  <li class="text-weight-bold">Bachelor of Engineering (IT)</li>
                </ul>
              </q-card-section>
            </q-card>
          </div>
        </div>
      </div>
    </div>

    <div class="contact-me" ref="contact">
      <div class="container">
        <div class="text-h4 text-weight-bold text-white text-center q-pb-xl contact-title">Contact Me</div>
        <div class="row justify-center q-col-gutter-lg q-mb-lg">
          <div class="col-12 col-sm-8 col-md-4 text-center">
            <q-icon size="lg" color="white" name="mail"/>
            <div class="text-subtitle1 text-weight-bold text-white q-mt-lg text-center">
              thutayarmoe97@gmail.com
            </div>
            <div class="text-subtitle1 text-weight-bold text-white q-mt-lg text-center">
            </div>
          </div>
          <div class="col-12 col-sm-8 col-md-4 text-center">
            <q-icon size="lg" color="white" name="phone"/>
            <div class="text-subtitle1 text-weight-bold text-white q-mt-lg text-center">
              +959 972 089 188
            </div>
          </div>
          <div class="col-12 col-sm-8 col-md-4 text-center">
            <q-icon size="lg" color="white" name="place"/>
            <div class="text-subtitle1 text-weight-bold text-white q-mt-lg text-center">
              No.(25), Bozinyaw 3rd street, 30 Quarter, North Dagon, Yangon.
            </div>
          </div>
        </div>
        <div class="line">
          <q-separator color="white" inset/>
        </div>
      </div>
    </div>

    <q-toolbar class="bg-primary text-dark text-center q-pa-lg">
      <div class="container">
        <q-row>
          <div class="text-dark text-subtitle1 text-weight-bold text-white">All rights reserved. Thuta Yar Moe</div>
          <q-icon @click="goto('facebook')" name="facebook" size="md" color="white" class="q-ma-md icons"/>
          <q-icon @click="goto('phone')" name="phone" size="md" color="white" class="q-ma-md icons"/>
          <q-icon @click="goto('mail')" name="mail" size="md" color="white" class="q-ma-md icons"/>
        </q-row>
      </div>
    </q-toolbar>

  </q-page>
</template>

<script>
import Projects from 'src/components/projects.vue';
import { defineComponent, ref, watch } from 'vue';

export default defineComponent({
  name: 'PageIndex',
  components: {
    Projects
  },
  props: {
    link: String
  },
  data() {
    return {
      technical: [
        { id: 1, name: 'Vue.js', percent: 0.8 },
        { id: 2, name: 'Nuxt JS', percent: 0.7 },
        { id: 3, name: 'Quasar', percent: 0.75 },
        { id: 4, name: 'Laravel', percent: 0.8 },
        { id: 5, name: 'PHP', percent: 0.78 },
        { id: 6, name: 'Javascript', percent: 0.73 },
      ],
      professional: [
        { id: 1, name: 'Teamwork', percent: 0.8 },
        { id: 2, name: 'Problem Solving', percent: 0.7 },
        { id: 3, name: 'Communication', percent: 0.6 },
        { id: 4, name: 'Creativity', percent: 0.75 },
      ]
    }
  },
  methods: {
    scrollToElement(val) {
      const el = this.$refs[val];
      if (el) {
        el.scrollIntoView({behavior: 'smooth'});
      }
    },

    goto(val) {
      if (val == 'facebook') window.open('https://www.facebook.com/thuta.yarmoe', '_blank');
      if (val == 'phone') window.open('tel:+959972089188', '_blank');
      if (val == 'mail') window.open('https://mail.google.com/mail/?view=cm&fs=1&to=thutayarmoe@icloud.com', '_blank');
    }
  },
  watch: {
    link(val) {
      if (val) {
        this.scrollToElement(val);
      }
    }
  }
})
</script>

<style lang="scss" scoped>
  .home {
    width: 100%;
    padding: 100px 0px;
    background: #efefef;
  }

  .about, .projects, .work-experience {
    width: 100%;
    padding: 90px 0px;
    background: #fff;
  }

  .whatido, .skills {
    width: 100%;
    padding: 90px 0px;
    background: #efefef;
  }

  .contact-me {
    width: 100%;
    padding: 90px 0px 0px;
    background: #2e8eaf;
    .contact-title {
      margin-bottom: 40px;
    }
  }

  .work-experience > li {
    line-height: 30px;
  }

  .container {
    width: 90%;
    max-width: 1000px;
    margin: 0 auto;
  }

  .hello {
    font-size: 14px;
    line-height: 24px;
    letter-spacing: 1px;
    font-weight: 700;
    padding: 10px 30px;
    border-top-left-radius: 20px;
    border-top-right-radius: 20px;
    border-bottom-right-radius: 20px;
    border-bottom-left-radius: 0;
    width: -webkit-fit-content;
    width: -moz-fit-content;
    width: fit-content;
    color: #fff;
  }

  .name {
    font-size: 46px;
    font-weight: bold !important;
    color: #000;
    margin: 20px 0 8px;
  }

  .profession {
    font-size: 24px;
    margin-bottom: 24px;
    color: #707070;
    font-weight: bold;
  }

  .what-i-do {
    padding: 40px;
    font-size: 25px;
  }
  .profile {
    .q-avatar {
      width: 300px;
      height: 300px;
      margin: auto;
      display: block;
      border: 3px solid #2e8eaf;
      overflow: hidden;
      box-shadow: 0px 3px 6px rgba(0,0,0,0.16);
    }
  }

  .my-info {
    display: flex;
    width: 100%;
    margin-bottom: 20px;
    .q-icon {
      font-size: 20px !important;
      line-height: 20px;
    }
    label {
      font-size: 15px;
      line-height: 20px;
      font-weight: normal !important;
      color: #000;
    }
  }

  .text-body1 {
    color: #000;
    font-weight: 500 !important;
  }

  .q-chip {
    border-top-left-radius: 10px;
    border-bottom-right-radius: 10px;
    padding: 16px;
  }

  .q-card {
    box-shadow: none !important;
    border: 2px solid #2e8eaf;
    // background: none !important;
    border-radius: 8px;
  }

  .q-card__section {
    ul {
      padding-left: 24px;
      line-height: 32px;
      color: #707070;
      font-size: 15px;
    }
  }

  .tech-value {
    color: #707070;
  }

  .icons {
    cursor: pointer;
  }

  .profile-image {
    object-fit: cover;
  }
</style>
