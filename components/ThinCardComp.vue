<template>
  <v-card
    class="rounded-xl"
    outlined
    color="black"
    rounded
  >
    <v-row>
      <v-col cols="9" xl="10" md="10" sm="9">
        <v-card-title style="font-weight: 600" class="text-uppercase pl-5 text-md-body-2" >
          {{ title }}
        </v-card-title>
      </v-col>
      <v-col cols="2" xl="2" md="2">
        <v-btn
          plain
          fab
          class="mt-2 ml-xl-3"
          small
        >
          <v-icon>
            mdi-chevron-right
          </v-icon>
        </v-btn>
      </v-col>
    </v-row>
    <v-row >
      <v-col cols="9" xl="9" md="7" sm="9">
        <v-card-title>
          <p :class="styling" style="font-weight: 600;">
            {{ bignum }}
          </p>
        </v-card-title>
      </v-col>
      <v-col cols="3" xl="3" md="5" sm="3">
        <v-btn
          fab
          x-small
          class="mt-4 mt-xl-8 mt-md-7 ml-md-15 ml-sm-12"
          plain
        >
          <v-icon color="#F8B400">
            mdi-chart-areaspline
          </v-icon>
        </v-btn>
      </v-col>
    </v-row>
  </v-card>
</template>

<script>
export default {
  name: 'ThinCardComp',
  components: {},
  props: {
    title: {
      type: String,
      default: null
    },
    bignum: {
      type: String,
      default: null,
    },
    styling:{
      type:String,
      default:null,
    }
  }
}
</script>
