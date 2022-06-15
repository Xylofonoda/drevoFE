<template>
  <v-app>
  <v-main>
    <v-app-bar color="#FFAB00" app>
      <v-row>
        <v-col cols="12" xl="2" md="2" sm="4">
          <v-row>
            <v-img
              style="background: black"
              src="/logo_white.svg"
              height="65px"
              contain
            ></v-img>
          </v-row>
        </v-col>
        <v-col class="d-none d-sm-block" xl="1" md="9" sm="8">
          <v-row style="position: relative;" class="ml-2">
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
            <v-col xl="8">
              <v-toolbar-title class=" mt-2 white--text text-uppercase" style="font-weight: 600; font-size: 15px;">
                {{ name }}
              </v-toolbar-title>
            </v-col>

          </v-row>
        </v-col>
      </v-row>
    </v-app-bar>

    <v-row no-gutters>
        <v-col cols="1" xl="2" sm="1" md="2" xs="0">
            <v-navigation-drawer
              permanent
              src="/bg.jpg"
              style="width: 100%"
              bottom
            >
              <v-list
                dense
                nav
              >
                <v-list-item
                  v-for="item in items"
                  :key="item.title"
                  :to="item.link"
                  link

                >
                  <v-list-item-icon>
                    <v-icon>{{ item.icon }}</v-icon>
                  </v-list-item-icon>
                  <v-list-item-content>
                    <v-list-item-title
                    >{{ item.title }}</v-list-item-title>
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
        {title: 'Přehled', link: '/admin/adminhome'},
        {title: 'Databáze'},
        {title: 'Plán', link: '/admin/adminplan'},
      ],
      name:"Přehled",
      right: null,
    }
  }

}
</script>


