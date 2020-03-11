<template>
  <v-content>
    <v-row class="d-flex justify-center align-center flex-row">
      <v-col cols="12" xs="12" sm="12" md="3" lg="3" class="order-xs-3 order-sm-3 order-md-1 order-lg-1">
        Left
      </v-col>
      <v-col cols="12" xs="12" sm="12" md="3" lg="6" class="order-xs-1 order-sm-1 order-md-2 order-lg-2">
        <Feed />
      </v-col>
      <v-col cols="12" xs="12" sm="12" md="3" lg="3" class="order-xs-2 order-sm-2 order-md-3 order-lg-3">
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
