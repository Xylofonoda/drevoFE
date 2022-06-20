<template>
  <v-card
    class="rounded-xl"
    outlined
    color="black"
    rounded
  >
    <v-row>
      <v-col cols="10">
        <v-card-title class="text-uppercase pl-5" style="font-size: 15px">
          {{ title }}
        </v-card-title>
      </v-col>
      <v-col cols="2">
        <v-btn
          plain
          fab
          class="mt-3"
          small
        >
          <v-icon>
            mdi-chevron-right
          </v-icon>
        </v-btn>
      </v-col>
    </v-row>
    <v-row no-gutters>
      <v-col cols="10" xl="10" md="10" sm="10">
        <v-card-title>
          <p class="pl-0 text-h4" style="font-weight: 600; ">
            {{ bignum }}
          </p>
        </v-card-title>
      </v-col>
      <v-col cols="2" xl="2" md="2" sm="10">
        <v-btn
          fab
          x-small
          class="mt-6 ml-6"
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
    }
  }
}
</script>
