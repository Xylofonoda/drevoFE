<template>
  <v-card
    class="rounded-xl"
    outlined
    :color="color"
    rounded
    :style="border"

  >
    <v-row>
      <v-col cols="10" xl="9" md="9" sm="10">
        <v-card-title style="font-weight: 600" class="text-uppercase pl-5 text-sm-body-2 text-md-body-2 text-xl-body-2" >
          {{ title }}
        </v-card-title>
      </v-col>
      <v-col cols="2" xl="3" md="3" sm="2">
        <v-btn
          plain
          fab
          class="mt-2 ml-xl-13 pr-md-3 ml-sm-2"
          small
        >
          <v-icon>
            mdi-chevron-right
          </v-icon>
        </v-btn>
      </v-col>
    </v-row>
    <v-row >
      <v-col cols="10" xl="9" md="7" sm="10" class="pa-0">
        <v-card-title>
          <p :class="styling" class="ml-md-4 mt-md-3" style="font-weight: 600;">
            {{ bignum }}
          </p>
        </v-card-title>
      </v-col>
      <v-col cols="2" xl="3" md="5" sm="2">
        <v-btn
          fab
          x-small
          class="mt-4 mt-xl-8 mt-md-7 px-sm-5 ml-md-12 pa-md-0 px-sm-6"
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
    },
    transparent:{
      type:Boolean,
      default:false
    }
  },
  computed:{
    color () {
      return this.transparent === true ? 'transparent' : 'black'
    },
    border () {
      return this.transparent === true ? 'border: 1px solid #ccc!important' : ''
    }
  }
}
</script>
