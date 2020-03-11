<template>
  <v-content>
    <v-row class="d-flex justify-center align-center flex-row">
      <v-col cols="12" xs="12" sm="12" md="2" lg="2" class="order-3 order-md-1 order-lg-1">
        Left
      </v-col>
      <v-col cols="12" xs="12" sm="12" md="6" lg="6" class="center-column order-1 order-sm-first order-md-1 order-lg-2">
        <Feed />
      </v-col>
      <v-col cols="12" xs="12" sm="12" md="2" lg="2" class="order-2 order-md-3 order-lg-3">
        Right
      </v-col>
    </v-row>
  </v-content>
</template>

<script>
// @ is an alias to /src
import Feed from '../components/Feed'

export default {
  name: 'home',
  components: {
    Feed
  }
}
</script>

<style scoped>
  .center-column {
    border-left: 1px solid #E0E2DB;
    border-right: 1px solid #E0E2DB;
  }
</style>
