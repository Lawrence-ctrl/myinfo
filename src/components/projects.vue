<template>
  <div class="text-h5 text-weight-bold text-center q-pb-lg">My Projects</div>
  <div class="row items-center justify-center">
    <div class="col-12 col-sm-8 col-md-12 q-py-md">
      <q-tabs
        v-model="tab"
        class="text-grey"
        active-color="primary"
        indicator-color="primary"
        align="justify"
        narrow-indicator
        no-caps
      >
        <q-tab name="website" label="Website" />
        <q-tab name="android" label="Android" />
        <q-tab name="ios" label="Ios" />
      </q-tabs>

      <q-tab-panels v-model="tab" animated>
        <q-tab-panel name="website" class="q-px-none">
          <website />
        </q-tab-panel>

        <q-tab-panel name="android">
          <android />
        </q-tab-panel>

        <q-tab-panel name="ios">
          <ios />
        </q-tab-panel>
      </q-tab-panels>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';
import website from './projects/website.vue';
import Ios from './projects/ios.vue';
import android from './projects/android.vue';
export default {
  components: { website, Ios, android },
  name: 'projects',
  setup() {
    return {
      tab: ref('website')
    }
  }
}
</script>

<style>

</style>
