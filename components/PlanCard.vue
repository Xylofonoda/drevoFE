<template>
  <v-row>
    <v-col>
      <v-card
        outlined
        rounded
        max-width="100%"
      >
        <v-row>
          <v-col cols="1">
            <v-checkbox

              class="pt-5 mx-2"
              color="black"
            ></v-checkbox>
          </v-col>
          <v-col cols="6">
            <v-card-title class="mx-2" style="font-size: 13px;">
              {{ evals }}
            </v-card-title>
            <v-card-subtitle style="font-size: 10px">
              <div class="rounded-pill elevation-2 mx-2" style="width: 60px">
                {{ save }}
              </div>
            </v-card-subtitle>
          </v-col>
          <v-col cols="5">
            <v-card-title
              style="font-size: 13px;"
              class="pt-8 ml-3 text-no-wrap"
            >
              <p class="text-right">
                1500 CZK
              </p>

            </v-card-title>
          </v-col>
        </v-row>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "PlanCardComponent",
  components: {},
  props: {
    evals: {
      type: String,
      default: null,
    },
    save: {
      type: String,
      default: null
    },
    checkboxOnce: {
      type: String,
      default: null,

    },
    // eslint-disable-next-line vue/require-default-prop,vue/require-prop-types
  }
}


</script>
