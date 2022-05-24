<template>
  <v-app fluid>
    <layout-component
      title="Název projektu"
    ></layout-component>
    <AccordComp>
    </AccordComp>
    <v-form>
      <v-list
        subheader
        two-line
      >
        <v-list-item
          v-for="folder in folders"
          :key="folder.title"
        >
          <v-col>
            <v-row>
              <v-list-item-icon>
                <v-icon
                  color="black"
                  class="pt-2"
                  size="30px"
                >mdi-folder
                </v-icon>
              </v-list-item-icon>
              <v-list-item-content>
                <v-list-item-title style="font-size:14px " v-text="folder.title"></v-list-item-title>

              </v-list-item-content>
              <v-list-item-action>
                <v-btn
                  icon
                  to=""
                >{{ folder.num }}
                  <v-icon
                    color="black"
                    size="30px"
                  >mdi-{{ `chevron-${miniVariant ? 'right' : 'right'}` }}
                  </v-icon>
                </v-btn>
              </v-list-item-action>
            </v-row>
            <v-divider class="mt-2"></v-divider>
          </v-col>
        </v-list-item>
      </v-list>
      <v-container>
        <v-btn
          block
          tile
          color="black"
          class="white--text"
        >Project report</v-btn>
      </v-container>

    </v-form>
    <p class="text-center">
      <v-btn
        outlined
        fab
        max-width="50px"
        max-height="50px"
        style="bottom: -260px"
        to="/app/project/createproject"
      >
        <v-icon
          size="50px"
        >mdi-plus
        </v-icon>
      </v-btn>
    </p>

  </v-app>
</template>

<script>
import LayoutComponent from "@/components/LayoutComp";

export default {
  name: "ShowProject",
  components: {LayoutComponent},
  layout: "ProjectsLayout",

  data: () => ({
    miniVariant: false,
    folders: [
      {
        title: 'Název podsložky (prvku)',
        num: 3,
      },
      {

        title: 'Trám 2B',
        num: 1,
      },

    ],
  }),
}
</script>

<style>
  html{
    overflow-y: hidden;
  }
</style>
