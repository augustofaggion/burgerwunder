<template>
  <AppNavbar />
  <AppHome />
  <AppMenu />
  <AppAbout />
  <AppLocation />
  <AppFooter />
</template>

<script>
import AppNavbar from './components/AppNavbar.vue'
import AppHome from './components/AppHome.vue'
import AppMenu from './components/AppMenu.vue'
import AppAbout from './components/AppAbout.vue'
import AppLocation from './components/AppLocation.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  name: 'App',
  components: {
    AppNavbar,
    AppHome,
    AppMenu,
    AppAbout,
    AppLocation,
    AppFooter
  }
}
</script>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
</style>
