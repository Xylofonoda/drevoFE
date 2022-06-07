<template>
    <v-app-bar color="#FFAB00" app>
      <v-row>
        <v-col cols="2">
          <v-row justify="start">
            <v-img
              style="background: black"
              src="/logo_white.svg"
              max-width="253px"
              height="65px"
              contain
            ></v-img>
          </v-row>
        </v-col>
        <v-col cols="10">
          <v-row style="position: relative;">
            <nuxt-link to="/admin/adminhome" style="text-decoration: none">
              <v-btn
                fab
                plain
                elevation="0"
                x-small
                class="mt-4"
                color="black"
              >
                <v-icon plain class="white--text" style="font-weight: 600; bottom: 2px">
                  mdi-{{ `chevron-${miniVariant ? 'left' : 'left'}` }}
                </v-icon>
              </v-btn>
            </nuxt-link>
            <v-toolbar-title class=" mt-5 white--text text-uppercase" style="font-weight: 600; font-size: 15px;">
              {{ name }}
            </v-toolbar-title>
          </v-row>
        </v-col>
      </v-row>
    </v-app-bar>
</template>

<script>
export default {
  name: "AdminToolComp",
  components: {},
  miniVariant: false,
  props: {
    name: {
      type: String,
      default: null
    }
  },
}
</script>
