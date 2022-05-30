<template>
  <v-card
    :class="radius"
    height="120px"
    width="130px"
    outlined
    rounded
    color="black"
    class="mx-3"
    link

  >
    <v-list-item four-line>
      <v-list-item-content>
        <v-list-item-title>
          <!--              Nazev karticky-->
          <p class="white--text" style="font-size: small">{{ label }}</p>
        </v-list-item-title>
      </v-list-item-content>
      <v-list-item-avatar
        class="mx-0"
        circle
        color="grey"
        size="25"
      ></v-list-item-avatar>
    </v-list-item>
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
    icons: {
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
