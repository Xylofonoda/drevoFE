<template>
  <v-app>
    <layout-comp title="About"></layout-comp>
    <v-row justify="center">
      <v-container>
        <v-expansion-panels accordion class="py-2">
          <v-expansion-panel
            v-for="accord in accords"
            :key="accord.title"
          >
            <v-expansion-panel-header class="py-7">
              <v-col cols="2">
                <v-icon
                  style="position:absolute; left: 14px; top: 25px"
                  size="30px"
                  color="black"
                >mdi-card-account-details
                </v-icon>
              </v-col>
              {{ accord.title }}
            </v-expansion-panel-header>
            <v-expansion-panel-content
            >
              <v-col cols="6" class="mx-auto">
                <p class="text-center">{{accord.desc}}</p>
              </v-col>
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-container>
      <v-col cols="12">
        <p style="color: gray;" class="text-center">
        </p>
      </v-col>
    </v-row>
  </v-app>
</template>

<script>
export default {
  name: "AboutPage",
  layout: "AllroundLayout",


  data: () => ({
    miniVariant: false,
    accords: [
      {
        title: 'Contacts',
        desc:"Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum "
      },
      {

        title: 'Project informations',
        desc:"Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum "
      },
      {

        title: 'Privacy policy',
        desc:"Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum "
      },
    ],
  }),
}
</script>
<style scoped>
 html{
   overflow-y: hidden;
 }
</style>
