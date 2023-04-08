<template>
  <div class="app">
    <TopNavigationVue class="app__nav"/>
    <div>About us</div>
    <FooterVue class="app__footer"/>
  </div>
</template>

<script>
import TopNavigationVue from '../components/nav/TopNavigation.vue'
import FooterVue from '../components/nav/Footer.vue'

export default {
  name: 'AboutPage',
  components: { TopNavigationVue, FooterVue },

  methods: {
    showInfo: () => {
        console.log('Witaj w konsoli')
        alert('Hello!')
    }
  }
}
</script>

<style scoped>
 .app {
  height: 100vh;
  min-height: 100vh;
  background-color: #C8D9EE;
 }

 .app__nav {
  position: sticky;
  top: 0;
 }

 .app__footer {
  position:fixed;
  bottom:0;
  width: 100%;
 }

</style>
