<template>
  <v-row justify="center">
    <v-container>
      <v-expansion-panels accordion class="py-2">
        <v-expansion-panel
          v-for="(item,i) in 3"
          :key="i"
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
            weqweqeq
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et
            dolore
            magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
            commodo
            consequat.
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-container>
  </v-row>
</template>

<script>
export default {
  name: "AboutPage",
  layout: "ProjectsLayout"
}
</script>
