<template>
  <v-app-bar fixed app>
    <v-row>
      <v-col cols="2">
        <v-toolbar-title
        >
          <nuxt-link to="/app/home" style="text-decoration: none">
            <v-btn
              fab
              elevation="0"
              small
              class="py-7"
            ><v-icon style="float: left" plain>mdi-{{ `chevron-${miniVariant ? 'left' : 'left'}` }}</v-icon>
            </v-btn>
          </nuxt-link>
        </v-toolbar-title>
      </v-col>
      <v-col cols="7">
        <v-toolbar-title class="py-3">
          {{ title }}
        </v-toolbar-title>
      </v-col>
      <v-col cols="2">
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
  },
  data: () => ({
    items: [
      { name: 'Přejmenovat' },
      { name: 'Smazat' },
    ],
    miniVariant: false,
  }),
}
</script>

