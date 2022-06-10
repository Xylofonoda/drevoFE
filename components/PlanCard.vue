<template>
  <v-item-group>
    <v-row>
      <v-col>
        <v-item v-slot="{ active, toggle }">
          <v-card
            :color="active ? '#F8B400' : ''"
            class="rounded-xl"
            :class="active ? 'black--text' : '' "
            outlined
            max-width="100%"
            max-height="80px"
            @click="toggle"
          >
            <v-row>
              <v-col cols="8">
                <v-row>
                  <v-card-title class="mx-3 mt-5" style="font-size: 13px;">
                    {{ evals }}
                  </v-card-title>
                </v-row>
                <v-row>
                  <v-card-subtitle style="font-size: 10px; position: relative; bottom: 40px">
                    <div class="rounded-pill accent elevation-2 mx-4 " style="width: 70px;">
                      <p style="color: white" class="text-center">{{ save }}</p>
                    </div>
                  </v-card-subtitle>
                </v-row>

              </v-col>
              <v-col cols="4">
                <v-card-title
                  style="font-size: 16px;"
                  class="pt-6 pr-1"
                >
                  <p class="text-right" style="font-weight: 600">
                    {{ price }}
                  </p>

                </v-card-title>
              </v-col>
            </v-row>

          </v-card>
        </v-item>
      </v-col>
    </v-row>
  </v-item-group>
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
    price: {
      type: String,
      default: null,
    },
    // eslint-disable-next-line vue/require-default-prop,vue/require-prop-types
  }
}
</script>
