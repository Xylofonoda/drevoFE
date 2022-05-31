<template>
  <v-card
    :class="radius"
    height="120px"
    width="130px"
    outlined
    elevation="4"
    rounded
    :color="color"
    class="mx-3"
    link

  >
    <v-row>
        <v-list-item two-line class="py-3">
          <v-list-item-content>
            <v-list-item-title class="pl-3">
              <!--              Nazev karticky-->
              <p class="white--text" style="font-size: small; font-weight: bold">{{ label }}</p>
            </v-list-item-title>
          </v-list-item-content>
          <v-list-item-avatar
            class="mr-3"
            circle
            color="grey"
            size="22"
            style="bottom: 8px"
            :icon="icon"
          ></v-list-item-avatar>
        </v-list-item>
      <v-list-item two-line class="py-3">
        <v-list-item-content>
          <v-list-item-title class="pl-3">
            <!--              Nazev karticky-->
            <p class="white--text" style="font-size: 40px;font-weight: bold; position: absolute; bottom: 40px">{{ number }}</p>
          </v-list-item-title>
        </v-list-item-content>

      </v-list-item>
    </v-row>

  </v-card>
</template>

<script>

export default {
  name: "CardComponent",
  components: {},
  props: {
    label: {
      type: String,
      default: null,

    },
    number: {
      type: String,
      default: null,

    },
    icon: {
      type: String,
      default: null,
      // mdiAccountCircleOutline
    },
    color: {
      type: String,
      default: null,
      // mdiAccountCircleOutline
    }
  },
  data: () => ({
    model: 3,
    rounded: [
      '0',
      'sm',
      'md',
      'lg',
      'xl',
      'pill',
      'circle',
    ],
  }),

  computed: {
    radius() {
      let rounded = 'rounded'
      const value = this.rounded[this.model]

      if (value !== 'md') {
        rounded += `-${value}`
      }

      return rounded
    },
  },

}
</script>
<style scoped>
.v-card--outlined >>> fieldset {
  border-color: black;
}
</style>
