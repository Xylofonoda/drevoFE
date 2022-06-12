<template>
<!--  <v-item-group>-->
    <v-row>
      <v-col>
        <v-item v-slot="{ active, toggle }">
          <v-card
            :color="active ? '#F8B400' : ''"
            class="rounded-xl"
            :class="{
              'black--text': active,
              'py-1': true,
              'px-4': true,
            }"
            outlined
            max-width="100%"
            @click="toggle"
          >
            <v-row
              style="min-height:100px"
            >
              <v-col cols="6" align-self="center">
                <p class="mb-0">{{ evals }}</p>
                <v-chip
                  v-if="save"
                  class="white--text"
                  x-small
                >
                  {{ save }}
                </v-chip>
              </v-col>
              <v-col cols="6" align-self="center">
                <p class="text-right mb-0" style="font-weight: 600">
                  {{ price }}
                </p>
              </v-col>
            </v-row>

          </v-card>
        </v-item>
      </v-col>
    </v-row>
<!--  </v-item-group>-->
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
