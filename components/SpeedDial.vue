<template>
  <v-speed-dial
    v-model="fab"
    :direction="direction"
    :transition="transition"
    bottom
    right
    fixed

  >
    <template #activator>
      <v-btn
        v-model="fab"
        color="#F8B400"
        fab
        style="float: right"
      >
        <v-icon v-if="fab" color="black">
          mdi-close
        </v-icon>
        <v-icon v-else color="black">
          mdi-chevron-up
        </v-icon>
      </v-btn>
    </template>
    <v-btn
      fab
      dark
      small
      to="/admin/account"
      color="#4d4d4d"
    >
      <v-card
        class="rounded"
        style="right: 20px"
        color="#4d4d4d"

      >
        <p class="my-1 mx-1 font-weight-regular text-lowercase">účet</p>
      </v-card>
      <v-icon class="mr-10">mdi-account</v-icon>
    </v-btn>
    <v-btn
      fab
      dark
      small
      color="#4d4d4d"
      to="/admin/nastaveni"

    >
      <v-card
        class="rounded"
        style="right: 23px"
        color="#4d4d4d"
        min-width="60px"
      >
        <p class="my-1 mx-1 font-weight-regular text-lowercase">nastavení</p>
      </v-card>
      <v-icon class="mr-16 pr-2">mdi-timer-sand-complete</v-icon>
    </v-btn>
    <v-btn
      fab
      dark
      small
      color="#F8B400"
      to="/admin/home"
    >
      <v-card
        class="rounded"
        style="right: 32px"
        color="#4d4d4d"
        min-width="60px"
      >
        <p class="my-1 mx-1 font-weight-regular text-lowercase">přidat poznámku</p>
      </v-card>
      <v-icon class="mr-16 pr-13">mdi-lightbulb</v-icon>
    </v-btn>
  </v-speed-dial>
</template>

<script>
export default {
  name: 'SpeedDial',
  components: {},
  data() {
    return {
      direction: 'top',
      fab: false,
      fling: false,
      hover: false,
      tabs: null,
      top: false,
      right: false,
      bottom: false,
      left: false,
      transition: 'slide-y-reverse-transition',

      watch: {
        top(val) {
          this.bottom = !val
        },
        right(val) {
          this.left = !val
        },
        bottom(val) {
          this.top = !val
        },
        left(val) {
          this.right = !val
        },
      },
    }
  },
}
</script>
