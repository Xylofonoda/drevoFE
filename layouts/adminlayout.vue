<template>
  <v-app>
  <v-main>
    <v-row no-gutters>
        <v-col cols="1" xl="2" sm="1" md="2" xs="0">
            <v-navigation-drawer
              permanent
              src="/bg.jpg"
              class="pr-7"
              bottom
            >
              <v-list
                dense
                nav
              >
                <v-list-item
                  v-for="item in items"
                  :key="item.title"
                  class="pt-3 "
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
        {title: 'Přehled'},
      ],
      right: null,
    }
  }

}
</script>


