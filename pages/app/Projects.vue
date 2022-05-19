<template>
  <v-app fluid>

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
              <v-list-item-title v-text="folder.title"></v-list-item-title>

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
    <v-btn
      outlined
      fab
      max-width="50px"
      max-height="50px"
      style="bottom: -260px"
      class="mx-auto"
      to=""
    >
      <v-icon
        size="50px"
      >mdi-plus
      </v-icon>
    </v-btn>
  </v-app>
</template>

<script>
export default {
  name: "ProjectsPage",
  layout: "ProjectsLayout",
  data: () => ({
    miniVariant:false,
    folders: [
      {
        title: 'Projekt 1',
        num: 33,
      },
      {

        title: 'Projekt2',
        num: 23,
      },
      {
        title: 'Projekt3',
        num: 10,
      },
    ],
  }),
}
</script>
