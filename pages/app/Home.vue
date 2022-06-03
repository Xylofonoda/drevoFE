<template>
  <v-row>
    <v-col xl="6">
      <nuxt-link
        to="/app/user-profile-view"
        style="text-decoration: none">
        <v-card
          :class="radius"
          height="120px"
          width="130px"
          outlined
          elevation="4"
          rounded
          color="black"
          class="mx-3"
          link
          style="background: transparent; border-style: solid; border-color: #F8B400"

        >
          <v-row>
            <v-list-item two-line class="py-2">
              <v-list-item-content>
                <v-list-item-title class="pl-3">
                  <p class="white--text text-uppercase font-weight-thin" style="font-size: small; ">Profil</p>
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-row>
              <v-list-item two-line class="py-1">
                <v-list-item-content>
                  <v-col cols="6">
                    <v-list-item-title>
                    </v-list-item-title>
                  </v-col>
                  <v-col cols="6">
                    <v-list-item-avatar
                      style="bottom: 20px"
                    >
                      <v-list-item-avatar
                        class="mr-0 pb-3"
                      >
                        <v-icon
                          color="#F8B400"
                          size="30"
                        >mdi-account
                        </v-icon>
                      </v-list-item-avatar>
                    </v-list-item-avatar>
                  </v-col>
                </v-list-item-content>
              </v-list-item>
            </v-row>
          </v-row>

          <!--          <v-row>-->
          <!--            <v-list-item two-line class="py-3">-->
          <!--              <v-list-item-content>-->
          <!--                <v-list-item-title class="pl-3">-->
          <!--                  &lt;!&ndash;              Nazev karticky&ndash;&gt;-->
          <!--                  <p class="white&#45;&#45;text font-weight-thin text-uppercase" style="font-size: small;">Profil</p>-->
          <!--                </v-list-item-title>-->
          <!--              </v-list-item-content>-->
          <!--            </v-list-item>-->
          <!--          </v-row>-->

        </v-card>
      </nuxt-link>
    </v-col>
    <v-col xl="6">
      <nuxt-link
        to="/app/plan"
        style="text-decoration: none">
        <CardComponent
          label="Plán"
          color="black"
          number="34"
          icon="mdi-archive"
        ></CardComponent>
      </nuxt-link>
    </v-col>
    <v-col xl="6">
      <nuxt-link
        to="/app/projects"
        style="text-decoration: none">
        <CardComponent
          label="Projekty"
          color="black"
          number="365"
          icon="mdi-folder-open"
        ></CardComponent>
      </nuxt-link>
    </v-col>
    <v-col xl="6">
      <nuxt-link
        to="/app/tutorials"
        style="text-decoration: none">
        <CardComponent
          label="Metodika"
          color="black"
          icon="mdi-lightbulb"
        ></CardComponent>
      </nuxt-link>
    </v-col>
    <v-col xl="6">
      <nuxt-link
        to="/app/hardware"
        style="text-decoration: none">
        <CardComponent
          label="Hardware"
          color="black"
          icon="mdi-toolbox"
        ></CardComponent>
      </nuxt-link>
    </v-col>
    <v-col xl="6">
      <nuxt-link
        to="/app/about"
        style="text-decoration: none">
        <v-card
          :class="radius"
          height="120px"
          width="130px"
          outlined
          elevation="4"
          rounded
          class="mx-3"
          link
          color="#FFAB00"

        >
          <v-row>
            <v-list-item two-line class="py-2">
              <v-list-item-content>
                <v-list-item-title class="pl-3">
                  <p class="black--text text-uppercase " style="font-size: small;font-weight: 500">O nás</p>
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-row>
              <v-list-item two-line>
                <v-list-item-content>
                  <v-col cols="7">
                    <v-list-item-title class="pl-3">
                      <p class="white--text" style="font-size: 30px;font-weight: bold; position:relative; bottom: 5px ">
                      </p>
                    </v-list-item-title>
                  </v-col>
                  <v-col cols="5">
                    <v-list-item-avatar
                      style="bottom: 20px"
                    >
                      <v-list-item-avatar
                        class="mr-0 pb-3"
                      >
                        <v-icon
                          color="white"
                          size="30"
                        >mdi-map-marker
                        </v-icon>
                      </v-list-item-avatar>
                    </v-list-item-avatar>
                  </v-col>
                </v-list-item-content>
              </v-list-item>
            </v-row>
          </v-row>
        </v-card>
      </nuxt-link>
    </v-col>
    <v-col xl="6">
      <nuxt-link
        to=""
        style="text-decoration: none">
        <v-card
          :class="radius"
          height="120px"
          width="130px"
          outlined
          elevation="4"
          rounded
          class="mx-3"
          link
          style="background: transparent; border-style: solid; border-color: #F8B400"

        >
          <v-row>
            <v-list-item two-line class="py-2">
              <v-list-item-content>
                <v-list-item-title class="pl-3">
                  <!--              Nazev karticky-->
                  <p class="white--text text-uppercase font-weight-thin " style="font-size: small; ">Queue</p>
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-row>
              <v-list-item two-line class="py-1">
                <v-list-item-content>
                  <v-col cols="7">
                    <v-list-item-title class="pl-2">
                      <p class="white--text" style="font-size: 30px;font-weight: bold; position: absolute; bottom: 55px">
                        3</p>
                    </v-list-item-title>
                  </v-col>
                  <v-col cols="5">
                    <v-list-item-avatar
                      style="bottom: 20px"
                    >
                      <v-list-item-avatar
                        class="mr-0 pb-3"
                      >
                        <v-icon
                          color="#F8B400"
                          size="30"
                        >mdi-timer-sand
                        </v-icon>
                      </v-list-item-avatar>
                    </v-list-item-avatar>
                  </v-col>
                </v-list-item-content>
              </v-list-item>
            </v-row>
          </v-row>
        </v-card>
      </nuxt-link>
    </v-col>


  </v-row>
</template>

<script>
import CardComponent from "@/components/CardComp";

export default {
  name: "HomePage",
  components: {CardComponent},
  layout: "HomeLayout",
  data: () => ({
    model: 3,
    rounded: [
      '0',
      'sm',
      'md',
      'lg',
      'xl',
      'pill',
      'circle',
    ],
  }),

  computed: {
    radius() {
      let rounded = 'rounded'
      const value = this.rounded[this.model]

      if (value !== 'md') {
        rounded += `-${value}`
      }

      return rounded
    },
  },

}
</script>
<style>
html {
  overflow-x: hidden;
  overflow-y: unset;
}

body {
  overflow-x: hidden;
  overflow-y: unset;
}

</style>
