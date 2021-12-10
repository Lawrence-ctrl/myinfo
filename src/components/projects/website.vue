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
            <q-carousel
              animated
              v-model="imageSlide"
              infinite
              :autoplay="autoplay"
              arrows
              transition-prev="slide-right"
              transition-next="slide-left"
              @mouseenter="autoplay = false"
              @mouseleave="autoplay = true"
            >
              <q-carousel-slide :name="1" img-src="https://cdn.quasar.dev/img/mountains.jpg" />
              <q-carousel-slide :name="2" img-src="https://cdn.quasar.dev/img/parallax1.jpg" />
              <q-carousel-slide :name="3" img-src="https://cdn.quasar.dev/img/parallax2.jpg" />
              <q-carousel-slide :name="4" img-src="https://cdn.quasar.dev/img/quasar.jpg" />
            </q-carousel>
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
      lorem: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque voluptatem totam, architecto cupiditate officia rerum, error dignissimos praesentium libero ab nemo provident incidunt ducimus iusto perferendis porro earum. Totam, numquam?'
    }
  }
}
</script>

