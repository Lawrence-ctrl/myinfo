<template>
  <div class="text-h4 text-weight-bolder text-center q-pb-lg">My Projects</div>
  <div class="row items-center justify-center">
    <div class="text-body2 q-mb-lg"> Here are some of the projects I have developed. </div>
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
        <q-tab color="dark" name="website" label="Website" />
        <q-tab color="dark" name="android" label="Android" />
        <q-tab color="dark" name="ios" label="IOS" />
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

<script setup>
import { ref } from 'vue'
import website from './projects/website.vue'
import Ios from './projects/ios.vue'
import android from './projects/android.vue'

const tab = ref('website')
</script>

<style>
</style>
