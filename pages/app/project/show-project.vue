<template>
  <v-app>
    <layout-comp
      title="Nazev projektu"
    ></layout-comp>
    <AccordComp
      name="Project Description"
      desc="Popis: Lorem Ipsum"
      gps="GPS: Lorem Ipsum"
      date-time="Datum: 2022-12-12"

    >
    </AccordComp>
    <v-form>
      <v-list
        subheader
        two-line
      >
        <v-list-item
          v-for="folder in folders"
          :key="folder.title"
          link
          to="/app/project/name-of-project"
          style="border-bottom: 1px solid gray"
        >
          <v-col>
            <v-row>
              <v-list-item-icon>
                <v-icon
                  color="#F8B400"
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
                  to="/app/project/name-of-project"
                >{{ folder.num }}
                  <v-icon
                    color="#F8B400"
                    size="30px"
                  >mdi-{{ `chevron-${miniVariant ? 'right' : 'right'}` }}
                  </v-icon>
                </v-btn>
              </v-list-item-action>
            </v-row>
          </v-col>
        </v-list-item>
      </v-list>
      <v-container>
        <v-btn
          block
          tile
          color="#F8B400"
          class="black--text"
        >Project report</v-btn>
      </v-container>

    </v-form>
    <v-row justify="center" class="ma-0">
      <v-btn
        outlined
        fab
        color="#F8B400"
        to="/app/project/tram-2b"
        fixed
        class="mb-16"
        bottom
      >
        <v-icon
          size="50px"
          color="#F8B400"
        >mdi-plus
        </v-icon>
      </v-btn>
    </v-row>
  </v-app>
</template>

<script>
import LayoutComp from "@/components/LayoutComp";

export default {
  name: "ShowProject",
  components: {LayoutComp},
  layout: "AllroundLayout",

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

