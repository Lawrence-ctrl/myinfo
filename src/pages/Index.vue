<template>
  <q-page>
    <div class="home">
      <div class="container">
        <div class="row items-center justify-center">
          <div class="col-12 col-sm-8 col-md-12">
            <div class="hello bg-primary">Hello I'm</div>
            <div class="name">THUTA YAR MOE</div>
            <div class="profession">Web Developer</div>
            <div class="text-body1 q-mb-sm">
              <q-icon name="mail" size="sm" class="q-mr-md" color="primary"/>
              thutayarmoe97@gmail.com
            </div>
            <div class="text-body1 q-mb-sm">
              <q-icon name="phone" size="sm" class="q-mr-md" color="primary"/>
              +959 972 089 188
            </div>
            <div class="text-body1 q-mb-sm">
              <q-icon name="place" size="sm" class="q-mr-md" color="primary"/>
              No.(25), Bozinyaw 3rd street, 30 Quarter, North Dagon, Yangon.
            </div>
          </div>
          <div class="col-6">

          </div>
        </div>
      </div>
    </div>

    <div class="about">
      <div class="container">
        <div class="text-h5 text-weight-bold text-center q-pb-lg">About Me</div>
        <div class="row items-center justify-center">
          <div class="col-12 col-sm-8">
            <div class="text-body1 text-weight-light ">
              Hi! I'm Thuta Yar Moe. I'm a Backend Developer.
              I studied Information Technology and graduated with bachelor of engineering (IT) from Technological University (Hmawbi).
              I'm very passionate and dedicated to my work. I enjoy every step of the development process, from discussion and collaboration.
              I have many experiences in website and mobile application development. I am good at
            </div>
            <div class="languages q-py-md">
              <q-chip outline square class="q-pa-md" size="md" color="primary" text-color="white">Vue.js</q-chip>
              <q-chip outline square class="q-pa-md" size="md" color="primary" text-color="white">NuxtJS</q-chip>
              <q-chip outline square class="q-pa-md" size="md" color="primary" text-color="white">Quasar</q-chip>
              <q-chip outline square class="q-pa-md" size="md" color="primary" text-color="white">Laravel</q-chip>
              <q-chip outline square class="q-pa-md" size="md" color="primary" text-color="white">PHP</q-chip>
              <q-chip outline square class="q-pa-md" size="md" color="primary" text-color="white">MySQL</q-chip>
              <q-chip outline square class="q-pa-md" size="md" color="primary" text-color="white">NGINX</q-chip>
              <q-chip outline square class="q-pa-md" size="md" color="primary" text-color="white">Digital Ocean</q-chip>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="whatido">
      <div class="container">
        <div class="text-h5 text-weight-bold text-center q-pb-xl">What I Do</div>
        <div class="row justify-center q-col-gutter-lg">
          <div class="col-12 col-sm-8 col-md-6">
            <q-card class="what-i-do text-center shadow-9">
              <q-card-section>
                <q-icon name="code" size="xl" class="q-mr-md"/>Web Development
              </q-card-section>
            </q-card>
          </div>
          <div class="col-12 col-sm-8 col-md-6">
            <q-card class="what-i-do text-center shadow-9">
              <q-card-section>
                <q-icon name="code" size="xl" class="q-mr-md"/>App Development
              </q-card-section>
            </q-card>
          </div>
        </div>
      </div>
    </div>

    <div class="projects">
      <div class="container">
        <Projects />
      </div>
    </div>

    <div class="skills">
      <div class="container">
        <div class="row justify-center q-col-gutter-x-lg">
          <div class="col-12 col-sm-8 col-md-5 q-mx-md q-mb-lg">
            <div class="text-h5 text-weight-bold text-center q-pb-xl">Technical Skills</div>
            <q-linear-progress v-for="tech in technical" :key="tech.id" :value="tech.percent" class="q-mt-md" />
          </div>
          <div class="col-12 col-sm-8 col-md-5 q-mx-md">
            <div class="text-h5 text-weight-bold text-center q-pb-xl">Professional Skills</div>
            <q-linear-progress v-for="pro in professional" :key="pro.id" :value="pro.percent" class="q-mt-md" />
          </div>
        </div>
      </div>
    </div>

    <div class="work-experience">
      <div class="container">
        <div class="row justify-center q-col-gutter-x-lg">
          <div class="col-12 col-sm-8 col-md-6 q-mb-lg">
            <div class="text-h5 text-weight-bold text-center q-pb-xl">Work Experience</div>

            <q-card class="q-mb-lg shadow-5">
              <q-card-section>
                <div class="text-h6 text-primary">YCDC</div>
                <ul>
                  <li>Junior Web Developer</li>
                  <li>Oct 2019 - Dec 2019 (Internship)</li>
                </ul>
              </q-card-section>
            </q-card>

            <q-card class="q-mb-lg shadow-5">
              <q-card-section>
                <div class="text-h6 text-primary">CGM</div>
                <ul>
                  <li>Junior Web Developer</li>
                  <li>Feb 2020 - May 2020 (Quit because of COVID 19)</li>
                </ul>
              </q-card-section>
            </q-card>

            <q-card class="q-mb-lg shadow-5">
              <q-card-section>
                <div class="text-h6 text-primary">Datalink</div>
                 <ul>
                  <li>Web Developer</li>
                  <li>July 2020 - July 2021</li>
                </ul>
              </q-card-section>
            </q-card>

          </div>
          <div class="col-12 col-sm-8 col-md-6">
            <div class="text-h5 text-weight-bold text-center q-pb-xl">Education</div>

            <q-card class="q-mb-lg shadow-5">
              <q-card-section>
                <div class="text-h6 text-primary">Technological University (HMAWBI)</div>
                <ul>
                  <li>2013 - 2019</li>
                  <li>Bachelor of Technology (IT)</li>
                  <li>Bachelor of Engineering (IT)</li>
                </ul>
              </q-card-section>
            </q-card>
          </div>
        </div>
      </div>
    </div>

  </q-page>
</template>

<script>
import Projects from 'src/components/projects.vue';
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'PageIndex',
  components: {
    Projects
  },
  setup() {
    let technical = [
      { id: 1, name: 'Vue.js', percent: 0.8 },
      { id: 2, name: 'Nuxt JS', percent: 0.7 },
      { id: 3, name: 'Quasar', percent: 0.75 },
      { id: 4, name: 'Laravel', percent: 0.8 },
      { id: 5, name: 'PHP', percent: 0.78 },
      { id: 6, name: 'Javascript', percent: 0.73 },
    ];
    let professional = [
      { id: 1, name: 'Teamwork', percent: 0.8 },
      { id: 2, name: 'Problem Solving', percent: 0.7 },
      { id: 3, name: 'Communication', percent: 0.6 },
      { id: 4, name: 'Creativity', percent: 0.75 },
    ];
    return {
      technical: ref(technical),
      professional: ref(professional)
    }
  }
})
</script>

<style scoped>
  .home {
    width: 100%;
    padding: 120px 0px;
    background: url('/assets/');
  }

  .about {
    width: 100%;
    padding: 120px 0px;
    background: #efefef;
  }

  .whatido {
    width: 100%;
    padding: 0px 0px 120px 0px;
    background: #efefef;
  }

  .projects {
    width: 100%;
    padding: 120px 0px;
    background: #ffffff;
  }

  .skills {
    width: 100%;
    padding: 120px 0px;
    background: #ffffff;
  }

  .work-experience {
    width: 100%;
    padding: 120px 0px;
    background: #efefef;
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
    font-size: 50px;
    font-weight: 700;
    line-height: 65px;
    margin-top: 10px;
    margin-bottom: 15px;
    opacity: .6;
    color: #000;
  }

  .profession {
    font-size: 26px;
    line-height: 34px;
    margin-bottom: 40px;
    opacity: .8;
    font-weight: 600;
  }

  .what-i-do {
    padding: 40px;
    font-size: 25px;
  }
</style>
