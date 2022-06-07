<template>
  <v-app>
  <v-main>
    <v-row no-gutters>
        <v-col cols="2">
            <v-navigation-drawer
              permanent
              src="/bg.jpg"
            >
              <v-list
                dense
                nav
              >
                <v-list-item
                  v-for="item in items"
                  :key="item.title"
                  link

                >
                  <v-list-item-icon>
                    <v-icon>{{ item.icon }}</v-icon>
                  </v-list-item-icon>
                  <v-list-item-content>
                    <v-list-item-title>{{ item.title }}</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </v-list>
            </v-navigation-drawer>
        </v-col>
        <v-col cols="10" class="mt-7">
          <Nuxt/>
        </v-col>
    </v-row>
  </v-main>
  </v-app>
</template>


<script>
export default {
  name: "AdminLayout",
  data() {
    return {
      fixed: false,
      miniVariant: false,
      items: [
        {title: 'Dashboard', icon: 'mdi-view-dashboard'},
        {title: 'Photos', icon: 'mdi-image'},
        {title: 'About', icon: 'mdi-help-box'},
      ],
      right: null,
    }
  }

}
</script>


