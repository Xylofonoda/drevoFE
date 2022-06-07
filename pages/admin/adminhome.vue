<template>
  <v-app>
    <admin-tool-comp
      name="Přehled">
    </admin-tool-comp>
    <v-container>
    <v-row>
      <v-col cols="4">
        <v-card
          class=""
          outlined
          color="black"
          rounded
          max-width="360px"
        >
          <v-row>
            <v-col cols="10">
              <v-card-title class="text-uppercase pl-5" style="font-size: 15px">
                Databáze
              </v-card-title>
            </v-col>
            <v-col cols="2">
              <v-btn
                plain
                fab
                class="pr-3"
              >
                <v-icon>
                  mdi-{{ `chevron-${miniVariant ? 'right' : 'right'}` }}
                </v-icon>
              </v-btn>
            </v-col>
          </v-row>
          <v-row>
            <v-col cols="8">
              <v-card-title>
                <p class="pl-1" style="font-weight: 600; font-size: 50px">
                  3 675
                </p>
              </v-card-title>
            </v-col>
            <v-col cols="4">
              <v-card-subtitle>
                <p class="pt-4 pl-2 font-weight-thin">Uživatelé</p>
              </v-card-subtitle>
            </v-col>
          </v-row>
        </v-card>
      </v-col>

    </v-row>
    </v-container>
  </v-app>
</template>

<script>
import AdminToolComp from "@/components/admintoolbar";

export default {
  name: "AdminHome",
  components: {AdminToolComp},
  layout: "adminlayout",
  data() {
    return {
      items: [
        {title: 'Dashboard', icon: 'mdi-view-dashboard'},
        {title: 'Photos', icon: 'mdi-image'},
        {title: 'About', icon: 'mdi-help-box'},
      ],
      right: null,
    }
  },
}
</script>
