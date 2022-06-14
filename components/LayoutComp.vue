<template>
  <v-app-bar fixed app>
    <v-row>
      <v-col cols="2" xl="1" md="1" sm="1">

          <nuxt-link to="/app/home" style="text-decoration: none">
            <v-btn
              fab
              elevation="0"
              small
              plain
              class="py-7"
              style="background: transparent"
            ><v-icon plain color="#F8B400">mdi-{{ `chevron-${miniVariant ? 'left' : 'left'}` }}</v-icon>
            </v-btn>
          </nuxt-link>
      </v-col>
      <v-col cols="8" xl="8" md="8" sm="8">
        <v-toolbar-title class="py-3">
          {{ title }}
        </v-toolbar-title>
      </v-col>
      <v-col v-if="items" cols="2">
        <v-menu>
          <template #activator="{ on, attrs }">
            <v-btn
              fab
              elevation="0"
              plain
              v-bind="attrs"
              color="black"
              small
              class="py-7"
              v-on="on"
            >
              <v-icon
                color="#F8B400"
              >mdi-dots-vertical
              </v-icon>
            </v-btn>
          </template>
          <v-list>
            <v-list-item
              v-for="(item, index) in items"
              :key="index"
              link
            >
              <v-list-item-title>{{ item.name }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
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
    items:{
      type: Array,
      default: null,
    }
  },
  data: () => ({
    miniVariant: false,
  }),
}
</script>

