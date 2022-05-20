<template>
  <v-container>
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
                to="/app/project/showproject"
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
  </v-container>
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
        where: "/app/project/showProject",
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

