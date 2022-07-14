<template>
    <v-row>
      <v-col>
        <v-item v-slot="{ active, toggle }">
          <v-card
            :style="active ? '' : 'background-color:black !important'"
            :color="active ? '#F8B400' : ''"
            class="rounded-lg bordercard"
            :class="{
              'black--text': active,
              'py-1': true,
              'px-4': true,
            }"
            outlined
            @click="toggle"
          >
            <v-row
              style="min-height:100px"
            >
              <v-col cols="6" xl="4" md="5" sm="3" align-self="center">
                <p class="mb-0">{{ evals }}</p>
                <v-chip
                  v-if="save"
                  class="white--text"
                  x-small
                >
                  {{ save }}
                </v-chip>
              </v-col>
              <v-col cols="6" xl="8" md="7" sm="9" xs="6" align-self="center">
                <p class="text-right mb-0" style="font-weight: 600">
                  <s style="color: gray">{{ pastPrice }} </s>{{ price }}
                </p>
              </v-col>
            </v-row>

          </v-card>
        </v-item>
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
    price: {
      type: String,
      default: null,
    },
    pastPrice:{
      type: String,
      default:null,
    }
    // eslint-disable-next-line vue/require-default-prop,vue/require-prop-types
  }
}
</script>
<style>
.bordercard{
  border-color: #696969 !important;


}
</style>
