<template>
  <v-app>
    <admin-tool-comp
      name="Přehled">
    </admin-tool-comp>
    <v-container class="ml-3 pr-10">
      <v-row>
        <v-col cols="12" xl="4" md="4" sm="12">
          <v-card
            class="rounded-xl"
            outlined
            color="black"
            rounded
            min-width="300px"

          >
            <v-row>
              <v-col cols="10" xl="10" md="10">
                <v-card-title class="text-uppercase pl-5" style="font-size: 15px">
                  Databáze
                </v-card-title>
              </v-col>
              <v-col cols="2">
                <v-btn
                  plain
                  fab
                  small
                  class=" mt-3"
                >
                  <v-icon>
                    mdi-{{ `chevron-${miniVariant ? 'right' : 'right'}` }}
                  </v-icon>
                </v-btn>
              </v-col>
            </v-row>
            <v-row>
              <v-col cols="7" xl="9" md="8" sm="9">
                <v-card-title>
                  <p class="pl-0 text-h4" style="font-weight: 600;">
                    3 675
                  </p>
                </v-card-title>
              </v-col>
              <v-col cols="5" xl="3" md="4" sm="3">
                <v-card-subtitle>
                  <p class="pt-4 font-weight-thin">Uživatelé</p>
                </v-card-subtitle>
              </v-col>
              <v-col cols="12" xl="12" md="12" sm="12">
                <v-card
                  class="mx-auto text-center"
                  color="black"
                  dark
                  max-width="600"
                >
                  <v-card-text>
                      <v-sparkline
                        :value="value"
                        :labels="labels"
                        color="#F8B400"
                        height="170"
                        width="450"
                        padding="24"

                      >

                      </v-sparkline>

                  </v-card-text>
                </v-card>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
        <v-col cols="12" xl="4" md="4" sm="12">


          <v-card
            class="rounded-xl"
            outlined
            color="black"
            rounded
            min-width="300px"

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
                  class="mt-3"
                  small
                >
                  <v-icon>
                    mdi-{{ `chevron-${miniVariant ? 'right' : 'right'}` }}
                  </v-icon>
                </v-btn>
              </v-col>
            </v-row>
            <v-row no-gutters>
              <v-col cols="10" xl="10" md="10" sm="10">
                <v-card-title>
                  <p class="pl-0 text-h4" style="font-weight: 600; ">
                    1 265 200
                  </p>
                </v-card-title>
              </v-col>
              <v-col cols="2" xl="2" md="2" sm="10">
                <v-btn
                  fab
                  x-small
                  class="mt-6 ml-6"
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
            min-width="300px"


          >
            <v-row>
              <v-col cols="10">
                <v-card-title class="text-uppercase pl-5 pb-3" style="font-size: 15px">
                  Hardware
                </v-card-title>
              </v-col>
              <v-col cols="2">
                <v-btn
                  plain
                  fab
                  class=" mt-3"
                  small
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
                  <p class="pl-1 text-h4" style="font-weight: 600; ">
                    12
                  </p>
                </v-card-title>
              </v-col>
              <v-col cols="2">
                <v-btn
                  fab
                  x-small
                  class="mt-6 ml-6 "
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
        <v-col cols="12" xl="4" md="4" sm="12">
          <v-card
            class="rounded-xl"
            outlined
            color="black"
            rounded
            min-width="300px"
          >
            <v-container>


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
                    small
                    class=" mt-3"
                  >
                    <v-icon>
                      mdi-{{ `chevron-${miniVariant ? 'right' : 'right'}` }}
                    </v-icon>
                  </v-btn>
                </v-col>
              </v-row>
              <v-row>
                <v-col xl="12" md="12" sm="12" xs="12">
                  <v-item-group>
                    <v-item>
                      <plan-card
                        evals="10 evaluations"
                        price="1500 Kč"
                      >
                      </plan-card>
                    </v-item>
                    <v-item>
                      <plan-card
                        evals="30 evaluations"
                        price="7000 Kč"
                        save="Save 20%"
                      >
                      </plan-card>
                    </v-item>
                    <v-item>
                      <plan-card
                        evals="50 evaluations"
                        save="Save 30%"
                        price="21000 Kč"
                      >
                      </plan-card>
                    </v-item>

                  </v-item-group>
                </v-col>
              </v-row>
            </v-container>
          </v-card>
        </v-col>
        <v-col cols="12" xl="4" md="4" sm="12">
          <v-card
            class="rounded-xl "
            color="transparent"
            style="border: 1px solid #ccc!important"
            rounded
            min-width="300px"
          >
            <v-container>


              <v-row>
                <v-col cols="10">
                  <v-card-title class="text-uppercase pl-5" style="font-size: 15px">
                    Uživatelé (stažení aplikace)
                  </v-card-title>
                </v-col>
                <v-col cols="2">
                  <v-btn
                    plain
                    fab
                    small
                    class="mt-3"
                  >
                    <v-icon>
                      mdi-{{ `chevron-${miniVariant ? 'right' : 'right'}` }}
                    </v-icon>
                  </v-btn>
                </v-col>
              </v-row>
              <v-row>
                <v-col xl="12" md="12" sm="12" xs="12">
                  <v-col cols="10">

                  </v-col>
                  <v-col cols="2">
                    <v-card-subtitle>

                    </v-card-subtitle>
                  </v-col>

                </v-col>
              </v-row>
            </v-container>
          </v-card>
        </v-col>
        <v-col cols="12" xl="4" md="4" sm="12">
          <v-card
            class="rounded-xl "
            color="transparent"
            style="border: 1px solid #ccc!important"
            rounded
            min-width="300px"
          >
            <v-container>
              <v-row>
                <v-col cols="10">
                  <v-card-title class="text-uppercase pl-5" style="font-size: 15px">
                    Uživatelé (podíl mutací)
                  </v-card-title>
                </v-col>
                <v-col cols="2">
                  <v-btn
                    plain
                    fab
                    small
                    class="mt-3"
                  >
                    <v-icon>
                      mdi-{{ `chevron-${miniVariant ? 'right' : 'right'}` }}
                    </v-icon>
                  </v-btn>
                </v-col>
              </v-row>
              <v-row>
                <v-col xl="12" md="12" sm="12" xs="12">
                  <v-col cols="10">

                  </v-col>
                  <v-col cols="2">
                    <v-card-subtitle>

                    </v-card-subtitle>
                  </v-col>

                </v-col>
              </v-row>
            </v-container>
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
  miniVariant: false,
  data() {
    return {
      items: [
        {title: 'Dashboard', icon: 'mdi-view-dashboard'},
        {title: 'Photos', icon: 'mdi-image'},
        {title: 'About', icon: 'mdi-help-box'},
      ],
      value: [
        423,
        446,
        675,
        510,
        590,
        610,
        760,
        590,
        675,
        423,
        760,
        960,
      ],
      labels:[
        "January",
        "February",
        "March",
        "April",
        "May",
        "June",
        "July",
        "August",
        "September",
        "October",
        "November",
        "December"
      ],
      right: null,
    }
  },
}
</script>
<style>
.rounded-card {
  border-radius: 100px;
}
</style>
