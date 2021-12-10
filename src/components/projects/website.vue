<template>
  <div>
    <q-carousel
      v-model="slide"
      transition-prev="slide-right"
      transition-next="slide-left"
      animated
      control-color="primary"
      class="rounded-borders"
    >
      <q-carousel-slide v-for="web in websites" :key="web.label" :name="web.value">
        <div class="row">
          <div class="col-12 col-md-8 col-lg-6 q-pa-md">
            <div class="text-h5 text-font-weight-bold q-mb-md">{{ web.name }}</div>

            <div class="text-body2 q-mb-lg">
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
          <div class="col-12 col-md-8 col-lg-6 q-pa-md">
            <q-img src="https://cdn.quasar.dev/img/mountains.jpg">
              <div class="absolute-bottom text-subtitle1 text-center">
                Caption
              </div>
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
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'
import websites from '../../json/websites.json';
export default {
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

