<template>
  <v-app>
  <v-form>
    <v-list
      subheader
      two-line
    >
      <v-list-item
        v-for="folder in folders"
        :key="folder.title"
        link

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
  </v-form>

  </v-app>
</template>
<script>
  export default {
    name:"FoldersComp",
    components:{},
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
