<template>
    <v-app-bar fixed app>
      <v-row>
        <v-col cols="3">
          <v-toolbar-title
          >
            <nuxt-link to="/app/home" style="text-decoration: none">
              <v-btn elevation="0">
                <v-icon style="float: left" plain>mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon>
              </v-btn>
            </nuxt-link>
          </v-toolbar-title>
        </v-col>
        <v-col cols="9">
          <v-toolbar-title class="py-1">
            {{title}}
          </v-toolbar-title>
        </v-col>
      </v-row>
    </v-app-bar>
</template>

<script>
export default {
  name: "LayoutComponent",
  components: {},
  props: {
    title: {
      type: String,
      default: null,
    },
  },
    data() {
      return {
        fixed: false,
        miniVariant: false,
      }
    }
}

</script>
