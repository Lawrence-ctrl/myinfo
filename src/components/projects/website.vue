<template>
  <div>
    <!-- <q-carousel
      v-model="slide"
      transition-prev="slide-right"
      transition-next="slide-left"
      animated
      control-color="primary"
      class="rounded-borders"
    >
      <q-carousel-slide q-carousel-slide v-for="web in websites" :key="web.label" :name="web.value">
        <div class="row">
          <div class="col-12 col-md-6 col-lg-6" :class="$q.screen.lt.sm ? 'q-mb-lg': ''">
            <div class="text-h5 text-weight-bold q-mb-md">{{ web.name }}</div>

            <div class="text-body2  q-mb-lg">
              {{ web.title }}
            </div>

            <div class="languages">
              <q-chip square color="primary" class="text-white" v-for="lang in web.languages" :key="lang">
                {{ lang }}
              </q-chip>
            </div>

            <q-btn no-caps color="primary" class="q-mt-lg" outline rounded @click="goto(web.link)">
              Go to Website
            </q-btn>
          </div>
          <div class="col-12 col-md-6 col-lg-6" :class="$q.screen.lt.sm ? 'q-mb-lg': ''">
            <q-img src="https://cdn.quasar.dev/img/mountains.jpg">
            </q-img>
          </div>
        </div>
      </q-carousel-slide>
    </q-carousel>

    <div class="row justify-center q-mt-md">
      <q-btn-toggle
        v-model="slide"
        :options="websites"
      />
    </div> -->
    <q-carousel
      v-model="slide"
      swipeable
      animated
      control-color="primary"
      padding
      arrows
      class="text-primary rounded-borders q-pb-none q-mb-none"
    >
      <q-carousel-slide class="column no-wrap flex-center q-mb-none" v-for="web in websites" :key="web.label" :name="web.value">
        <q-avatar size="56px" square>
          <img :src="web.logo" />
        </q-avatar>
        <div class="q-mt-md text-center text-black" style="min-width: 300px">
          <div class="text-h5 text-weight-bold q-mb-md">{{ web.name }}</div>

          <div class="text-body2  q-mb-lg">
            {{ web.title }}
          </div>

          <div class="languages q-mb-lg">
            <q-chip color="primary" outline class="text-primary" v-for="lang in web.languages" :key="lang">
              {{ lang }}
            </q-chip>
          </div>

          <q-btn no-caps color="primary" class="q-mt-md q-mr-sm" flat v-if="web.type == 'admin'">
            {{ web.platform }}
          </q-btn>

          <q-btn no-caps color="primary" class="q-mt-md q-mr-sm" v-if="web.showLink" @click="goto(web.link)">
            Go to Website
          </q-btn>

          <light-box v-if="web.showImg" :link="web.link" :images="web.images" />
        </div>
      </q-carousel-slide>
    </q-carousel>

    <div class="row justify-center q-mt-none q-pt-none">
      <q-btn-toggle
        v-model="slide"
        :options="websites"
      />
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'
import websites from '../../json/websites.json';
import LightBox from '../light-boxes.vue';
export default {
  components: {
    LightBox
  },
  setup () {
    async function goto(link) {
      window.open(link, '_blank');
    }

    return {
      goto,
      websites: websites,
      autoplay: ref(false),
      imageSlide: ref(1),
      slide: ref('jobsharmal'),
    }
  }
}
</script>

