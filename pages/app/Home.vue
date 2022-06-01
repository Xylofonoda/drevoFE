<template>
  <v-row>
    <v-col xl="6">
      <nuxt-link
        to="/app/userprofileview"
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

        >
          <v-row>
            <v-list-item two-line class="py-3">
              <v-list-item-content>
                <v-list-item-title class="pl-3">
                  <!--              Nazev karticky-->
                  <p class="white--text" style="font-size: small; font-weight: bold">Profile</p>
                </v-list-item-title>
              </v-list-item-content>
              <v-list-item-avatar
                class="mr-3"
                size="25"
                style="bottom: 10px"
              >
                <v-icon
                  color="white"
                  size="30"
                >mdi-account-circle
                </v-icon>
              </v-list-item-avatar>
            </v-list-item>
          </v-row>

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
          number="36"
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
        ></CardComponent>
      </nuxt-link>
    </v-col>
    <v-col xl="6">
      <nuxt-link
        to="/app/about"
        style="text-decoration: none">
        <CardComponent
          label="About"
          color="black"
        ></CardComponent>
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

        >
          <v-row>
            <v-list-item two-line class="py-3">
              <v-list-item-content>
                <v-list-item-title class="pl-3">
                  <!--              Nazev karticky-->
                  <p class="black--text" style="font-size: small; font-weight: bold">Queue</p>
                </v-list-item-title>
              </v-list-item-content>
              <v-list-item-avatar
                class="mr-3"
                circle
                color="grey"
                size="22"
                style="bottom: 10px"
              ></v-list-item-avatar>
            </v-list-item>
            <v-list-item two-line class="py-3">
              <v-list-item-content>
                <v-list-item-title class="pl-3">
                  <!--              Nazev karticky-->
                  <p class="black--text" style="font-size: 40px;font-weight: bold; position: absolute; bottom: 40px">
                    3</p>
                </v-list-item-title>
              </v-list-item-content>

            </v-list-item>
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
  overflow-y: unset
;
}

</style>
