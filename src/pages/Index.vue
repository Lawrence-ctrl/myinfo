<template>
  <q-page>
    <div class="home" ref="home">
      <div class="container">
        <div class="row items-center justify-center">
          <div class="col-sm-12 col-md-6" :class="$q.screen.lt.sm ? 'q-mb-xl': ''">
            <div class="hello bg-primary">Hello I'm</div>
            <div class="name">THUTA YAR MOE</div>
            <div class="profession">Full Stack Developer</div>
            <div class="text-body1 q-mb-sm my-info">
              <q-icon name="mail" size="sm" class="q-mr-md" color="primary"/>
              <label>thutayarmoe97@gmail.com</label>
            </div>
            <div class="text-body1 q-mb-sm my-info">
              <q-icon name="phone" size="sm" class="q-mr-md" color="primary"/>
              <label>+959 972 089 188, +63 906 015 8406</label>
            </div>
            <div class="text-body1 q-mb-sm my-info">
              <q-icon name="place" size="sm" class="q-mr-md" color="primary"/>
              <label>Unit 4424 The Baecon Condo Arnaiz Tower Chino Roces Ave Makati City, Philippines</label>
            </div>
          </div>
          <div class="col-md-6 col-sm-12">
            <div class="profile">
              <q-avatar>
                <img src="thutayarmoe.jpeg" class="profile-image">
              </q-avatar>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="about" ref="about">
      <div class="container">
        <!-- Section Title -->
        <div class="text-h4 text-center text-weight-bolder q-pb-lg">
          “ About Me ”
        </div>

        <!-- Row to Center Content -->
        <div class="row items-center justify-center">
          <div class="col-12 col-sm-8">
            <!-- Introduction Text -->
            <div class="text-body1 q-mb-lg">
              <p>
                Hi, I’m <strong>Thuta Yar Moe</strong>, a passionate and dedicated
                <strong>Backend Developer</strong> from Myanmar. I earned my Bachelor of Engineering in
                Information Technology from <strong>Technological University (Hmawbi)</strong>.
              </p>
              <p>
                I am currently based in the Philippines, where I work as a
                <strong>Senior Backend Developer</strong>. My passion lies in creating efficient and scalable solutions,
                and I thrive in collaborative environments where ideas transform into impactful projects.
              </p>
              <p>
                Over the years, I’ve gained extensive experience in website and mobile application development,
                completing numerous projects that blend functionality and design. I specialize in using a variety
                of tools and frameworks, including <strong>Docker</strong>, <strong>Nginx</strong>,
                <strong>React</strong>, <strong>React Native</strong>, <strong>Vue</strong>, <strong>Quasar</strong>,
                <strong>Laravel</strong>, <strong>PHP</strong>, <strong>MySQL</strong>, <strong>FastAPI</strong>, and <strong>Python</strong>.
                I am committed to continuous learning and applying my skills to deliver high-quality solutions
                that meet user needs.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="whatido">
      <div class="container">
        <div class="text-h4 text-center text-weight-bolder q-pb-xl">What I Do</div>
        <div class="row justify-center q-col-gutter-lg">

          <!-- Web Development Section -->
          <div class="col-12 col-sm-8 col-md-6">
            <q-card class="what-i-do text-center shadow-9 hover-effect">
              <q-card-section>
                <q-avatar size="70px" rounded class="q-mr-sm">
                  <img src="~/assets/website3.png" alt="Web Development Icon" />
                </q-avatar>
                <div class="text-h5 text-weight-bold q-mt-md">Web Development</div>
                <p class="q-mt-sm">
                  Crafting dynamic, responsive, and secure websites tailored to your needs. My expertise includes integrating:
                  <ul class="text-left q-mt-lg">
                    <li>Payment Gateways (Stripe, PayPal, etc.)</li>
                    <li>Single Sign-On (SSO) for seamless authentication</li>
                  </ul>
                </p>
              </q-card-section>
            </q-card>
          </div>

          <!-- Mobile Development Section -->
          <div class="col-12 col-sm-8 col-md-6">
            <q-card class="what-i-do text-center shadow-9 hover-effect">
              <q-card-section>
                <q-avatar size="70px" rounded class="q-mr-sm">
                  <img src="~/assets/app.png" alt="Mobile Development Icon" style="object-fit:contain"/>
                </q-avatar>
                <div class="text-h5 text-weight-bold q-mt-md">Mobile Development</div>
                <p class="q-mt-sm">
                  Building robust backend solutions for mobile applications. I ensure:
                  <ul class="text-left q-mt-lg">
                    <li>Secure data handling with optimized APIs</li>
                    <li>Integration with third-party tools (e.g., push notifications, in-app purchases)</li>
                    <li>Scalable and efficient backend architecture</li>
                  </ul>
                </p>
              </q-card-section>
            </q-card>
          </div>

          <!-- API Development Section -->
          <div class="col-12">
            <q-card class="what-i-do text-center shadow-9 hover-effect">
              <q-card-section>
                <q-avatar size="70px" rounded class="q-mr-sm">
                  <img src="~/assets/app.png" alt="API Development Icon" style="object-fit:contain"/>
                </q-avatar>
                <div class="text-h5 text-weight-bold q-mt-md">API Development</div>
                <p class="q-mt-sm">
                  I design and implement APIs tailored to your business needs. Features include:
                  <ul class="text-left q-mt-lg">
                    <li>Optimized performance for high-traffic applications</li>
                    <li>Advanced data security and encryption protocols</li>
                  </ul>
                </p>
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

    <!-- <div class="skills">
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
    </div> -->

    <div class="work-experience">
      <div class="container">
        <div class="row justify-center q-col-gutter-x-lg">
          <div class="col-12 col-sm-8 col-md-6 q-mb-lg">
            <div class="text-h4 text-weight-bolder text-center q-pb-xl">Work Experience</div>
            <q-timeline>
              <q-timeline-entry
                v-for="(experience, index) in workExperience"
                :key="index"
                :title="experience.company"
                :subtitle="experience.position"
                :body="experience.duration"
                icon="work"
                color="primary"
              >
                <!-- <div class="text-weight-bold">{{ experience.position }}</div>
                <div class="text-weight-bold">{{ experience.duration }}</div> -->
              </q-timeline-entry>
            </q-timeline>
          </div>

          <div class="col-12 col-sm-8 col-md-6">
            <div class="text-h4 text-weight-bolder text-center q-pb-xl">Education</div>
            <q-timeline>
              <q-timeline-entry
                v-for="(education, index) in education"
                :key="index"
                :title="education.institution"
                :subtitle="education.degree"
                :body="education.duration"
                icon="school"
                color="primary"
              >
                <!-- <div class="text-weight-bold">{{ education.degree }}</div> -->
              </q-timeline-entry>
            </q-timeline>
          </div>
        </div>
      </div>
    </div>

    <div class="certificates" ref="certificates">
      <div class="container">
        <div class="col-12 col-sm-8 col-md-6 q-mb-lg">
          <div class="text-h4 text-weight-bolder text-center q-pb-xl">Certificates</div>
            <q-timeline>
              <q-timeline-entry
                v-for="(certificate, index) in certificates"
                :key="index"
                :subtitle="certificate.issuer"
                :body="certificate.date"
                icon="verified"
                color="primary"
              >
              <template v-slot:title>
                <div
                  class="cursor-pointer text-weight-bold text-underline"
                  @click="goto('certificate', certificate.link)"
                >
                  {{ certificate.title }}
                </div>
              </template>
                <!-- <div class="text-weight-bold">{{ certificate.title }}</div>
                <div class="text-weight-bold">{{ certificate.issuer }}</div>
                <div class="text-weight-bold">{{ certificate.date }}</div> -->
              </q-timeline-entry>
            </q-timeline>
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
            <div class="text-subtitle1 text-weight-bold text-white text-center">
              +63 906 015 8406
            </div>
          </div>
          <div class="col-12 col-sm-8 col-md-4 text-center">
            <q-icon size="lg" color="white" name="place"/>
            <div class="text-subtitle1 text-weight-bold text-white q-mt-lg text-center">
              Unit 4424 The Baecon Condo Arnaiz Tower Chino Roces Ave Makati City, Philippines
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
        <div class="text-dark text-subtitle1 text-weight-bold text-white">All rights reserved. Thuta Yar Moe</div>
        <!-- <q-icon @click="goto('facebook')" name="facebook" size="md" color="white" class="q-ma-md icons"/>
        <q-icon @click="goto('phone')" name="phone" size="md" color="white" class="q-ma-md icons"/>
        <q-icon @click="goto('mail')" name="mail" size="md" color="white" class="q-ma-md icons"/> -->
      </div>
    </q-toolbar>
  </q-page>
</template>

<script>
import Projects from 'src/components/projects.vue';
import { defineComponent } from 'vue';

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
      workExperience: [
        {
          company: 'CGM Golden Land',
          position: 'Junior Web Developer',
          duration: 'Feb 2020 - May 2020'
        },
        {
          company: 'Datalink',
          position: 'Web Developer',
          duration: 'June 2020 - July 2021'
        },
        {
          company: 'Spiceworks Myanmar & WIT Lab (Philippines)',
          position: 'Senior Full-Stack Developer',
          duration: 'Jan 2022 - present'
        }
      ],
      education: [
        {
          institution: 'Technological University (HMAWBI)',
          degree: 'Bachelor of Technology (IT)',
          duration: '2013 - 2017'
        },
        {
          institution: 'Technological University (HMAWBI)',
          degree: 'Bachelor of Engineering (IT)',
          duration: '2017 - 2019'
        }
      ],
      certificates: [
        {
          title: 'Certified Mid-Level Vue.js Developer',
          issuer: 'certificates.dev',
          date: 'May 12, 2025',
          link: 'https://certificates.dev/vuejs/certificates/9ee45070-7f33-4f3a-8867-afbc1b310067'
        },
        {
          title: 'Certified Senior Vue.js Developer',
          issuer: 'certificates.dev',
          date: 'May 27, 2025',
          link: 'https://certificates.dev/vuejs/certificates/9f0332d7-e7ab-46b9-9c77-293c4144fb84'
        }
      ],
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

    goto(val, link = null) {
      if (val === 'facebook') window.open('https://www.facebook.com/thuta.yarmoe', '_blank');
      if (val === 'phone') window.open('tel:+959972089188', '_blank');
      if (val === 'mail') window.open('https://mail.google.com/mail/?view=cm&fs=1&to=thutayarmoe@icloud.com', '_blank');
      if (val === 'certificate') window.open(link)
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

  .whatido, .skills, .certificates {
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

  .text-underline {
    text-decoration: underline;
  }
</style>
