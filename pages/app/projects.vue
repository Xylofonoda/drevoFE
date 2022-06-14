<template>
  <v-app>
    <layout-comp
      title="Projects"
      :items="[
      { name: 'Přejmenovat' },
      { name: 'Smazat' },
    ]"
    ></layout-comp>

    <v-list
      subheader
      two-line
      name="projects"
    >
      <v-list-item
        v-for="folder in folders"
        :key="folder.title"
        link
        to="/app/project/show-project"
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
              <v-list-item-title v-text="folder.title"></v-list-item-title>

            </v-list-item-content>
            <v-list-item-action>
              <v-btn
                icon
                to="/app/project/show-project"
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
    <v-row justify="center" class="ma-0">
      <v-btn
        outlined
        fab
        to="/app/project/create-project"
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
  name: "ProjectsPage",
  layout: "AllroundLayout",
  data: () => ({
    miniVariant: false,
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

<style scoped>
html {
  overflow-y: hidden;
}


</style>
