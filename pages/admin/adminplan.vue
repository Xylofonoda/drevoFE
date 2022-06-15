<template>
  <v-app>
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
            <v-container class="my-xl-1">
              <v-row>
                <v-col cols="10" xl="10" md="9" >

                  <v-card-title class="text-uppercase pl-5" style="font-size: 15px">
                    Plán
                  </v-card-title>
                </v-col>
                <v-col cols="2" xl="2" md="3">
                  <v-btn
                    plain
                    fab
                    small
                    class="mt-3"
                  >
                    <v-icon>
                      mdi-chevron-right
                    </v-icon>
                  </v-btn>
                </v-col>
              </v-row>
              <v-row no-gutters>
                <v-col cols="12" xl="12" md="12" sm="12">
                  <v-card
                    v-for="item in packages"
                    :key="item.title"
                    color="black"
                    min-width="300px"
                  >
                    <v-card-title
                      class="text-xl-body-1 text-md-body-1 text-sm-body-2"
                      style="color: gray"
                    >
                      {{item.title}}
                    </v-card-title>
                    <v-card-subtitle
                      class="white--text text-xl-h5 text-md-body-1 text-sm-body-2"
                      style="font-weight: 600"
                    >
                      {{item.price}}
                    </v-card-subtitle>
                    <v-row class="float-end pr-5">
                      <v-col cols="2" xl="2" md="4">
                        <v-btn
                          fab
                          small
                          plain
                        >
                          <v-icon color="#F8B400">
                            {{ item.icon }}
                          </v-icon>
                        </v-btn>
                      </v-col>
                    </v-row>
                 </v-card>


<!--                  <v-card-title class="text-xl-body-1 text-md-body-1 text-sm-body-2" style="color: gray">-->
<!--                    Balík měření #1 CZE-->
<!--                  </v-card-title>-->
<!--                  <v-card-subtitle class="text-xl-h5 text-md-body-1 text-sm-body-2" style="font-weight: 600">-->
<!--                    10ks / 1500Kč-->
<!--                  </v-card-subtitle>-->
<!--                  <v-card-title class="text-xl-body-1 text-md-body-1 text-sm-body-2" style="color: gray">-->
<!--                    Balík měření #2 CZE-->
<!--                  </v-card-title>-->
<!--                  <v-card-subtitle class="text-xl-h5 text-md-body-1 text-sm-body-2" style="font-weight: 600">-->
<!--                    50ks / <s>7500Kč</s> 6000Kč-->
<!--                  </v-card-subtitle>-->
<!--                  <v-card-title class="text-xl-body-1 text-md-body-1 text-sm-body-2" style="color: gray">-->
<!--                    Balík měření #3 CZE-->
<!--                  </v-card-title>-->
<!--                  <v-card-subtitle class="text-xl-h5 text-md-body-1 text-sm-body-2" style="font-weight: 600">-->
<!--                    20ks / <s>30000Kč</s> 2100Kč-->

                </v-col>
              </v-row>
            </v-container>
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
            <v-row no-gutters class="my-xl-8">
              <v-col cols="10">
                <v-card-title class="text-uppercase pl-5" style="font-size: 15px">
                  Otazník
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
                    mdi-chevron-right
                  </v-icon>
                </v-btn>
              </v-col>
            </v-row>
            <v-row class="my-2 ">
              <v-col cols="12">
                <v-row class="pl-4">
                  <v-col cols="3" xl="3" md="3">
                    <nuxt-link to="" class="white--text text-md-body-2">Otazník CZE</nuxt-link>
                  </v-col>
                  <v-col cols="4" xl="4" md="4">
                    <nuxt-link to="" class="white--text text-md-body-2">Questionmark ENG</nuxt-link>
                  </v-col>
                  <v-col cols="4" xl="4" md="4">
                    <nuxt-link to="" class="white--text text-md-body-2">Fragezeichen GER</nuxt-link>
                  </v-col>
                </v-row>
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
            <v-row no-gutters class="my-xl-5">
              <v-col cols="10">
                <v-card-title class="text-uppercase " style="font-size: 15px">
                  Vyfakturovano
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
                    mdi-chevron-right
                  </v-icon>
                </v-btn>
              </v-col>
            </v-row>
            <v-row no-gutters>
              <v-col cols="10" xl="10" md="10" sm="10">
                <v-card-title>
                  <p class="text-xl-h3 text-md-h4 text-sm-h5" style="font-weight: 600; ">
                    1 265 200
                  </p>
                </v-card-title>
              </v-col>
              <v-col cols="2" xl="2" md="2" sm="2">
                <v-btn
                  fab
                  x-small
                  class="mt-8 ml-1"
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
            <v-row no-gutters class="my-xl-5">
              <v-col cols="10">
                <v-card-title class="text-uppercase pl-5" style="font-size: 15px">
                  historie plateb
                </v-card-title>
              </v-col>
              <v-col cols="2">
                <v-btn
                  plain
                  fab
                  class="mt-2"
                  small
                >
                  <v-icon>
                    mdi-chevron-right
                  </v-icon>
                </v-btn>
              </v-col>
            </v-row>
            <v-row no-gutters>
              <v-col cols="12">
                <v-card-title>
                  <p class="text-xl-h5 text-md-h6" style="font-weight: 600;position:relative; top: 20px ">
                    26 672
                  </p>
                </v-card-title>
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
            <v-row no-gutters class="my-xl-4 pb-xl-1">
              <v-col cols="10">
                <v-card-title class="text-uppercase pl-5" style="font-size: 15px">
                  Platební metody
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
                    mdi-chevron-right
                  </v-icon>
                </v-btn>
              </v-col>
            </v-row>
            <v-row no-gutters>
              <v-col cols="12" xl="12" md="12" sm="12">
                <v-card-title>
                  <p class="pt-1 text-xl-h3 text-md-h4" style="font-weight: 600; ">
                    2
                  </p>
                </v-card-title>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
        <v-col cols="12" xl="4" md="4" sm="12">
          <v-card
            class="rounded-xl"
            outlined
            color="gray"
            rounded
            min-width="300px"
            min-height="150px"
            link
          >
            <p class="text-center my-16">
              <v-btn
                outlined
                fab
                disabled

              >
                <v-icon
                  size="50px"
                  class="mx-auto"
                >mdi-plus
                </v-icon>
              </v-btn>
            </p>

          </v-card>
        </v-col>
      </v-row>
      <v-row class="pt-xl-5 pt-md-3">
        <v-col cols="4">
          <p class="text-start text-uppercase text-xl-h6 mt-xl-3" style="font-weight: 600">
            historie plateb
          </p>
        </v-col>
        <v-col cols="4">
          <v-card
            outlined
            color="gray"
          >
            <v-row>
              <v-col cols="12">
                <v-text-field
                  class="px-4 my-0 text-uppercase"
                  label="hledat"
                  append-icon="mdi-magnify"
                  color="gray"
                >
                </v-text-field>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
        <v-col cols="4">
            <v-row class="float-end my-xl-2" align="center">
                <v-switch
                  color="#F8B400"
                >
                </v-switch>
                <p class="text-xl-subtitle-2 my-0">
                  S platbou
                </p>
              <v-btn
                color="white"
                small
                fab
                plain
              >
                <v-icon>
                  mdi-dots-vertical
                </v-icon>
              </v-btn>
            </v-row>
          <v-col cols="4">

          </v-col>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>

export default {
  name: "AdminPlan",
  layout: "adminlayout",
  miniVariant: false,
  data() {
    return {
      packages: [
        {title: 'Balík měření #1 CZE', price: '10ks / 1500Kč'},
        {title: 'Balík měření #2 CZE', price: '50ks / 6000Kč'},
        {title: 'Balík měření #3 CZE', price: '10ks / 1500Kč', icon:'mdi-chart-areaspline' },

      ],
    }
  },
}
</script>

