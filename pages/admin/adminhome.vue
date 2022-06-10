<template>
  <v-app>
    <admin-tool-comp
      name="Přehled">
    </admin-tool-comp>
    <v-container>
      <v-row>
        <v-col cols="4">
          <v-card
            class="rounded-xl"
            outlined
            color="black"
            rounded
            max-width="500px"
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
                  class="pr-5"
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
        <v-col cols="4" xl="4">
          <v-card
            class="rounded-xl"
            outlined
            color="black"
            rounded
            max-width="500px"
            height="130px"
          >
            <v-row>
              <v-col cols="10">
                <v-card-title class="text-uppercase pl-5" style="font-size: 15px">
                  Fakturace
                </v-card-title>
              </v-col>
              <v-col cols="2">
                <v-btn
                  plain
                  fab
                  class="pr-5"
                >
                  <v-icon>
                    mdi-{{ `chevron-${miniVariant ? 'right' : 'right'}` }}
                  </v-icon>
                </v-btn>
              </v-col>
            </v-row>
            <v-row no-gutters>
              <v-col cols="10">
                <v-card-title>
                  <p class="pl-1" style="font-weight: 600; font-size: 50px">
                    1 265 200
                  </p>
                </v-card-title>
              </v-col>
              <v-col cols="2">
                <v-btn
                  fab
                  x-small
                  class="mt-6 ml-4"
                  plain
                >
                  <v-icon color="#F8B400">
                    mdi-chart-areaspline
                  </v-icon>
                </v-btn>
              </v-col>
            </v-row>
          </v-card>
          <v-spacer class="mt-3"></v-spacer>
          <v-card
            class="rounded-xl"
            outlined
            color="black"
            rounded
            max-width="500px"
            height="130px"
          >
            <v-row>
              <v-col cols="10">
                <v-card-title class="text-uppercase pl-5" style="font-size: 15px">
                  Hardware
                </v-card-title>
              </v-col>
              <v-col cols="2">
                <v-btn
                  plain
                  fab
                  class="pr-5"
                >
                  <v-icon>
                    mdi-{{ `chevron-${miniVariant ? 'right' : 'right'}` }}
                  </v-icon>
                </v-btn>
              </v-col>
            </v-row>
            <v-row no-gutters>
              <v-col cols="10">
                <v-card-title>
                  <p class="pl-1" style="font-weight: 600; font-size: 50px">
                    12
                  </p>
                </v-card-title>
              </v-col>
              <v-col cols="2">
                <v-btn
                  fab
                  x-small
                  class="mt-6 ml-4"
                  plain
                >
                  <v-icon color="#F8B400">
                    mdi-chart-areaspline
                  </v-icon>
                </v-btn>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
        <v-col cols="4" xl="4">
          <v-card
            class="rounded-xl"
            outlined
            color="black"
            rounded
            max-width="500px"
          >
            <v-row>
              <v-col cols="10">
                <v-card-title class="text-uppercase pl-5" style="font-size: 15px">
                  Plán
                </v-card-title>
              </v-col>
              <v-col cols="2">
                <v-btn
                  plain
                  fab
                  class="pr-5"
                >
                  <v-icon>
                    mdi-{{ `chevron-${miniVariant ? 'right' : 'right'}` }}
                  </v-icon>
                </v-btn>
              </v-col>
            </v-row>
            <v-row>
              <v-col cols="12">
                <v-container>
                  <plan-card
                    evals="10 evaluations"
                    price="1500 Kč"
                  >
                  </plan-card>
                  <plan-card
                    evals="30 evaluations"
                    price="7000 Kč"
                    save="Save 20%"
                  >
                  </plan-card>
                  <plan-card
                    evals="50 evaluations"
                    save="Save 30%"
                    price="21000 Kč"
                  >
                  </plan-card>
                </v-container>
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
<style>
  .rounded-card{
    border-radius:100px;
  }
</style>
