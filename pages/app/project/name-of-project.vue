<template>
  <v-app>
    <layout-comp
      title="Trám 2B"
    ></layout-comp>

    <v-expansion-panels>
      <v-expansion-panel>
        <v-expansion-panel-header class="py-6">
          <v-col cols="2">
            <v-icon
              style="position:absolute; left: 14px; top: 20px"
              size="30px"
              color="#F8B400"
            >mdi-square-edit-outline
            </v-icon>
          </v-col>
          Subproject description
        </v-expansion-panel-header>
        <v-expansion-panel-content>

        </v-expansion-panel-content>
      </v-expansion-panel>
    </v-expansion-panels>
    <nuxt-link to="/app/project/mereni02" style="text-decoration: none">
    <v-list
      subheader
      two-line
    >
      <v-list-item
        v-for="folder in folders"
        :key="folder.title"
        link
        style="border-bottom: 1px solid gray"

      >
        <v-col>
          <v-row>
            <v-list-item-icon>
              <v-icon
                color="#F8B400"
                class="pt-2"
                size="30px"
              >mdi-chart-areaspline
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
    </nuxt-link>
    <v-row justify="center" class="ma-0">
      <v-btn
        outlined
        fab
        to="/app/project/tram-2b"
        fixed
        color="#F8B400"
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
  export default {
    name:"NameOfProject",
    layout:"AllroundLayout",
    data: () => ({
      miniVariant: false,
      folders: [
        {
          title: 'Measurement 01'
        },
        {

          title: 'Měření 02',
        },

      ],
    }),
  }
</script>

