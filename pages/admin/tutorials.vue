<template>
  <v-app>
    <v-container>
      <v-row>
        <v-col
          v-for="item in cards"
          :key="item.cardtitle"
          cols="12"
          xl="4"
          md="4"
          sm="12">
          <thin-card-comp
            :title="item.cardtitle"
            :bignum="item.bignum"
            :transparent='item.transparent'
            :styling="item.styling"
          ></thin-card-comp>
        </v-col>
        <v-col cols="12" xl="4" md="4" sm="12">
          <v-card
            class="rounded-xl"
            outlined
            color="gray"
            rounded
            min-width="300px"
            link
          >
            <p class="text-center my-16">
              <v-btn
                outlined
                fab
                disabled

              >
                <v-icon
                  size="50px"
                  class="mx-auto"
                >mdi-plus
                </v-icon>
              </v-btn>
            </p>
          </v-card>
        </v-col>
        <v-col
          cols="12"
          xl="4"
          md="4"
          sm="12"
        >
          <v-card
            height="100%"
            class="rounded-xl"
            color="black"
          >
            <v-card-title class="text-h6 black--text amber darken-1">
              Metodiky CZE
            </v-card-title>

            <v-card-text>
              <v-list color="black">
                <v-list-item
                  v-for="(folder, index) in folders"
                  :key="folder.title"
                  link
                  style="border-bottom: 1px solid gray"
                >
                  <v-col>
                    <v-row>
                      <v-list-item-avatar>
                        <v-icon
                          color="white"
                        >mdi-file
                        </v-icon>
                      </v-list-item-avatar>
                      <v-list-item-content>
                        <v-list-item-title style="font-weight: bold" v-text="folder.title"></v-list-item-title>
                        <v-list-item-subtitle v-text="folder.subtitle"></v-list-item-subtitle>
                      </v-list-item-content>
                      <v-list-item-action>
                        <v-row>
                          <v-btn
                            icon
                            download
                            href="file.pdf"
                          >
                            <v-icon
                              color="white"
                            >mdi-download
                            </v-icon>
                          </v-btn>
                          <v-btn
                            icon
                            @click="deleteFolder(index)"
                          >
                            <v-icon
                              color="white"
                            >mdi-close
                            </v-icon>
                          </v-btn>
                        </v-row>
                      </v-list-item-action>
                    </v-row>
                  </v-col>
                </v-list-item>
              </v-list>
            </v-card-text>
            <p class="text-center my-16">
              <v-btn
                outlined
                fab
                color="grey"
              >
                <v-icon
                  size="50px"
                  class="mx-auto"
                >mdi-plus
                </v-icon>
              </v-btn>
            </p>
            <v-divider></v-divider>

            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn
                color="#F8B400"
                text
              >
                Uložit
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
      <speed-dial>
      </speed-dial>
    </v-container>
  </v-app>
</template>
<script>
export default {
  name: 'AdminTutorials',
  components:{},
  layout: 'adminlayout',
  data() {
    return {
      cards: [
        {
          cardtitle: 'metodiky cze',
          bignum: '2',
          styling: 'text-xl-h3 text-md-h3 text-sm-h3 ml-sm-3 text-h3 ml-3 mb-xl-2',
          transparent: true
        },
        {
          cardtitle: 'Tutorials',
          bignum: '2',
          styling: 'text-xl-h3 text-md-h3 text-sm-h3 ml-sm-3 text-h3 ml-3 mb-xl-2'
        },
        {
          cardtitle: 'Anwesungen GER',
          bignum: '2',
          styling: 'text-xl-h3 text-md-h3 text-sm-h3 ml-sm-3 text-h3 ml-3 mb-xl-2'
        }
      ],
      folders: [
        {
          title: 'Lorem Ipsum sit dolor: PDF',
          subtitle: 'Language:CZE'
        },
        {
          title: 'Lorem Ipsum s: PDF',
          subtitle: 'Language:CZE'
        }
      ],
    }
  },

  methods: {
    deleteFolder(index) {
      this.folders.splice(index, 1);
    },
  }
}

</script>
