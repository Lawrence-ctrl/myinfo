<template>
  <div class="q-py-md">
    <q-carousel
      v-model="slide"
      transition-prev="slide-right"
      transition-next="slide-left"
      animated
      control-color="primary"
      class="rounded-borders"
    >
      <q-carousel-slide v-for="app in android" :key="app.label" :name="app.value">
        <div class="row">
          <div class="col-12 col-md-8 col-lg-6 q-pa-md">
            <div class="text-h5 text-font-weight-bold q-mb-md">{{ app.name }}</div>

            <div class="text-body2 q-mb-lg">
              {{ app.title }}
            </div>

            <div class="languages">
              <q-chip square color="primary" class="text-white" v-for="lang in app.languages" :key="lang">
                {{ lang }}
              </q-chip>
            </div>

            <q-btn no-caps color="primary" class="q-mt-lg" outline rounded @click="goto(app.link)">
              Download {{ app.name }}
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
        :options="android"
      />
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'
import android from '../../json/android.json';
export default {
  setup () {
    async function goto(link) {
      window.open(link, '_blank');
    }

    return {
      goto,
      android: android,
      slide: ref('jobsharmal'),
      lorem: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque voluptatem totam, architecto cupiditate officia rerum, error dignissimos praesentium libero ab nemo provident incidunt ducimus iusto perferendis porro earum. Totam, numquam?'
    }
  }
}
</script>
