<template>
  <v-app>
    <v-app-bar color="#FFAB00" app>
      <v-row>
        <v-col cols="2">
          <v-img
            class="justify-start"
            style="left: -10px"
            src="/adminlogo.png"
            max-width="219px"

            contain
          ></v-img>
        </v-col>
        <v-col cols="10">
          <v-row class="pt-3" style="position: relative; left: -35px">
            <nuxt-link to="/admin/adminhome" style="text-decoration: none">
              <v-btn
                fab
                plain
                elevation="0"
                x-small
                class="mt-4"
                color="black"
              >
                <v-icon plain class="white--text" style="font-weight: 600;">
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
  </v-app>
</template>

<script>
export default {
  name: "AdminToolComp",
  components: {},
  miniVariant: false,
  layout: "AllroundLayout",
  props: {
    name: {
      type: String,
      default: null
    }
  },
}
</script>
