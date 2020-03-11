<template>
  <v-app>
    <Header v-if="authToken"/>
    <router-view></router-view>
    <Footer v-if="authToken"/>
  </v-app>
</template>

<script>
import Header from './components/shared/Header'
import Footer from './components/shared/Footer'

export default {
  name: 'App',

  components: {
    Header,
    Footer
  },

  data: () => ({
    authToken: false
  })
}
</script>
