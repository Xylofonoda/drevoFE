<!--<template>-->
<!--    <v-app-bar color="#FFAB00" app>-->
<!--      <v-row>-->
<!--        <v-col cols="12" xl="2" md="2" sm="4">-->
<!--          <v-row>-->
<!--            <v-img-->
<!--              style="background: black"-->
<!--              src="/logo_white.svg"-->
<!--              height="65px"-->
<!--              contain-->
<!--            ></v-img>-->
<!--          </v-row>-->
<!--        </v-col>-->
<!--        <v-col class="d-none d-sm-block" xl="10" md="9" sm="8">-->
<!--          <v-row style="position: relative;" class="ml-2">-->
<!--            <nuxt-link to="/admin/adminhome" style="text-decoration: none">-->
<!--              <v-btn-->
<!--                fab-->
<!--                plain-->
<!--                elevation="0"-->
<!--                x-small-->
<!--                class="mt-4"-->
<!--                color="black"-->
<!--              >-->
<!--                <v-icon plain class="white&#45;&#45;text" style="font-weight: 600; bottom: 2px">-->
<!--                  mdi-{{ `chevron-${miniVariant ? 'left' : 'left'}` }}-->
<!--                </v-icon>-->
<!--              </v-btn>-->
<!--            </nuxt-link>-->
<!--            <v-col cols="3">-->

<!--            </v-col>-->
<!--            <v-toolbar-title class=" mt-5 white&#45;&#45;text text-uppercase" style="font-weight: 600; font-size: 15px;">-->
<!--              {{ name }}-->
<!--            </v-toolbar-title>-->
<!--          </v-row>-->
<!--        </v-col>-->
<!--      </v-row>-->
<!--    </v-app-bar>-->
<!--</template>-->

<script>
export default {
  name: "AdminToolComp",
  components: {},
  miniVariant: false,
  props: {
    name: {
      type: String,
      default: null
    }
  },
}
</script>
