<template>
  <v-app fluid>
    <layout-component
      title="Tutorial"
    ></layout-component>
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
            <v-list-item-avatar>
              <v-icon
                class="grey lighten-1"
                dark
              >mdi-file
              </v-icon>
            </v-list-item-avatar>
            <v-list-item-content>
              <v-list-item-title style="font-weight: bold" v-text="folder.title"></v-list-item-title>
              <v-list-item-subtitle v-text="folder.subtitle"></v-list-item-subtitle>
            </v-list-item-content>
            <v-list-item-action>
              <v-btn
                icon
                download
                href="file.pdf"
              >
                <v-icon
                  color="black"
                >mdi-download
                </v-icon>
              </v-btn>
            </v-list-item-action>
          </v-row>
          <v-divider class="mt-2"></v-divider>
        </v-col>
      </v-list-item>
    </v-list>
  </v-app>
</template>
<!--roboto condensed -->
<script>
import LayoutComponent from "@/components/LayoutComp";
export default {
  name: "TutorialsPage",
  components: {LayoutComponent},
  layout: "TutorialLayout",
  data: () => ({
    folders: [
      {
        subtitle: 'Language: CZE',
        title: 'Lorem ipsum dolor sit ame',
      },
      {
        subtitle: 'Language: CZE',
        title: 'Lorem ipsum dolor sit ame',
      },
      {
        subtitle: 'Language: CZE',
        title: 'Lorem ipsum dolor sit ame',
      },
    ],
  }),
}
</script>
