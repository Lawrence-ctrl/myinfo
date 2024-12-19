<template>
  <div class="q-py-md">
    <q-carousel
      v-model="slide"
      swipeable
      animated
      control-color="primary"
      padding
      arrows
      class="text-primary rounded-borders q-pb-none q-mb-none"
    >
      <q-carousel-slide class="column no-wrap flex-center q-mb-none" v-for="app in android" :key="app.label" :name="app.value">
        <q-avatar size="56px" square>
          <img :src="app.logo" />
        </q-avatar>
        <div class="q-mt-md text-center text-black" style="min-width: 300px">
          <div class="text-h5 text-weight-bold q-mb-md">{{ app.name }}</div>
          <div class="text-body2  q-mb-lg">
            {{ app.title }}
          </div>
          <div class="languages q-mb-lg">
            <q-chip color="primary" outline class="text-primary" v-for="lang in app.languages" :key="lang">
              {{ lang }}
            </q-chip>
          </div>
          <q-btn no-caps color="primary" class="q-mt-md q-mr-sm" @click="goto(app.link)" v-if="app.uploaded">
            Download App
          </q-btn>
          <q-btn no-caps color="primary" class="q-mt-md q-mr-sm"  v-if="!app.uploaded">
            Pending ...
          </q-btn>
          <light-box v-if="app.showImg" :link="app.link" :images="app.images" />
        </div>
      </q-carousel-slide>
    </q-carousel>

    <div class="row justify-center q-mt-none q-pt-none">
      <q-btn-toggle
        v-model="slide"
        :options="android"
      />
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import android from '../../json/android.json';
import LightBox from '../light-boxes.vue';
const slide = ref('jobsharmal');
const goto = async(link) => {
  window.open(link, '_blank');
}
</script>
