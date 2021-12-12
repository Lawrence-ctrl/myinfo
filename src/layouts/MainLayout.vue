<template>
  <q-layout view="hHh Lpr lFf">
    <q-header>
      <div class="container gt-sm">
        <q-toolbar class="q-py-md">
          <q-toolbar-title>MyInfo</q-toolbar-title>
          <div>
            <q-btn flat @click="scrollToElement('home')">Home</q-btn>
            <q-btn flat @click="scrollToElement('about')">About</q-btn>
            <q-btn flat @click="scrollToElement('projects')">Projects</q-btn>
            <q-btn flat @click="scrollToElement('contact')">Contact</q-btn>
          </div>
        </q-toolbar>
      </div>

      <q-toolbar class="lt-md">
        <q-btn flat round dense icon="menu" class="q-mr-sm" @click="toggleLeftDrawer"/>
        <q-toolbar-title class="absolute-center">MyInfo</q-toolbar-title>
      </q-toolbar>
    </q-header>
    <q-drawer
      class="lt-md"
      v-model="leftDrawerOpen"
      overlay
    >
      <q-list padding>
        <q-item clickable @click="scrollToElement('home')">
          <q-item-section avatar>
            <q-icon color="primary" name="home" />
          </q-item-section>

          <q-item-section>
            Home
          </q-item-section>
        </q-item>

        <q-item clickable @click="scrollToElement('about')">
          <q-item-section avatar>
            <q-icon color="primary" name="info" />
          </q-item-section>

          <q-item-section>
            About
          </q-item-section>
        </q-item>

        <q-item clickable @click="scrollToElement('projects')">
          <q-item-section avatar>
            <q-icon color="primary" name="list" />
          </q-item-section>

          <q-item-section>
            Projects
          </q-item-section>
        </q-item>

        <q-item clickable @click="scrollToElement('contact')">
          <q-item-section avatar>
            <q-icon color="primary" name="contact_page" />
          </q-item-section>

          <q-item-section>
            Contact
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view :link="link"/>
    </q-page-container>
  </q-layout>
</template>

<script>


import { defineComponent } from 'vue'

export default defineComponent({
  name: 'MainLayout',

  data() {
    return {
      link: null,
      leftDrawerOpen: false,
    }
  },

  methods: {
    scrollToElement(url) {
      this.leftDrawerOpen = false;
      this.link = url;
    },
    toggleLeftDrawer () {
      this.leftDrawerOpen = !this.leftDrawerOpen
    }
  },

  watch: {
    "$q.screen.width"() {
      if (this.$q.screen.gt.sm) {
        this.leftDrawerOpen = false;
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
