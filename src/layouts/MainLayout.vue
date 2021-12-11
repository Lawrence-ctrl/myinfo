<template>
  <q-layout view="hHh Lpr lFf">
    <q-header elevated>
      <div class="container">
        <q-toolbar class="q-py-md">
          <q-toolbar-title>MyInfo</q-toolbar-title>

           <q-btn flat @click="scrollToElement('home')">Home</q-btn>
           <q-btn flat @click="scrollToElement('about')">About</q-btn>
           <q-btn flat @click="scrollToElement('projects')">Projects</q-btn>
           <q-btn flat @click="scrollToElement('contact')">Contact</q-btn>
        </q-toolbar>
      </div>
    </q-header>
    <q-drawer
      class="lt-md"
      v-model="leftDrawerOpen"
      bordered
    >
      <q-list>
        <q-item-label
          header
        >
          Essential Links
        </q-item-label>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view :link="link"/>
    </q-page-container>
  </q-layout>
</template>

<script>


import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'MainLayout',

  setup () {
    const link = ref(null);
    const leftDrawerOpen = ref(false);

    function scrollToElement(url) {
      link.value = url;
    }

    return {
      link,
      scrollToElement,
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>

<style scoped>
.container {
  width: 90%;
  max-width: 1000px;
  margin: 0 auto;
}
.q-toolbar__title {
  font-weight: bold !important;
  color: #fff !important;
}
.q-btn {
  text-transform: initial !important;
  color: #fff !important;
}
</style>
