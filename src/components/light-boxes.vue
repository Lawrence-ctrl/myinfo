<template>
  <q-btn no-caps color="primary" class="q-mt-md" @click="showImages">
    View Images
  </q-btn>
  <vue-easy-lightbox
    :visible="visible"
    :imgs="images"
    :index="index"
    @hide="handleHide"
  ></vue-easy-lightbox>
</template>

<script>
import { defineComponent } from 'vue';
export default defineComponent({
  props: {
    link: {
      required: true,
    },
    images: {
      required: true
    }
  },
  name: 'light box',
  data() {
    return {
      visible: false,
      index: 0, // default: 0
    }
  },
  methods: {
    showImages() {
      this.index = 0;
      this.visible = true
    },
    handleHide() {
      this.visible = false
    }
  }
});
</script>

<style>

</style>
