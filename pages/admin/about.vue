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
            :icon="item.icon"
            :icon-right="item.iconRight"
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
              Project information
            </v-card-title>
            <v-card-text>
              <v-col>
                <v-row>
                  <v-row>
                    <v-expansion-panels
                      class="mt-5"
                    >
                      <v-expansion-panel
                        v-for="item in expansion"
                        :key="item.expatitle"
                        class="black mx-2"
                        style="border-bottom: 1px solid white!important;"

                      >
                        <v-expansion-panel-header>
                          {{ item.expatitle }}
                        </v-expansion-panel-header>
                        <v-expansion-panel-content>
                          {{ item.expacontent }}
                        </v-expansion-panel-content>
                      </v-expansion-panel>
                      <v-row>
                        <v-col cols="12">
                          <v-select
                              v-model="firstSelect"
                              class="mx-6 ma-0 mt-3"
                              color="white"
                              label="Verze: "
                              :items="items"

                            >
                            </v-select>
                          <v-select
                            v-model="secondSelect"
                            class="mx-6 ma-0"
                            color="white"
                            label="Copyright: "
                            :items="secondItems"
                          >
                          </v-select>
                        </v-col>
                      </v-row>
                    </v-expansion-panels>
                  </v-row>
                </v-row>
              </v-col>
            </v-card-text>
            <v-divider></v-divider>

            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn
                color="white"
                text
                class="pt-0"
                @click="clearForm"


              >
                Close
              </v-btn>
              <v-btn
                color="#F8B400"
                text
              >
                Save
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>
<script>
export default {
  name: 'AdminAbout',
  components: {},
  layout: 'adminlayout',
  data() {
    return {
      cards: [
        {
          // Card contents
          cardtitle: 'Contacts',
          bignum: 'Lorem ipsum s.r.o.',
          styling: 'text-xl-h4 text-md-h4 text-sm-h4 ml-sm-3  pb-md-0 text-h3 ml-3 mb-xl-2',
          transparent: false,
          icon: false,
          iconRight: true
        },
        {
          cardtitle: 'Project version',
          bignum: '1.0.0 (50)',
          styling: 'text-xl-h4 text-md-h4 text-sm-h4 ml-sm-3 text-h3 ml-3 mb-xl-2',
          transparent: true,
          icon: false,
          iconRight: true
        },
        {
          cardtitle: 'Users logged in',
          bignum: '2',
          styling: 'text-xl-h4 text-md-h4 text-sm-h4 ml-sm-3 text-h3 ml-3 mb-xl-2',
          icon: false,
          iconRight: true
        }
      ],
      // Accordion component filled with lorem ipsum
      expansion: [
        {
          expatitle: 'Description',
          expacontent: 'tivn?? v??pl??ov?? text p??i vytv????en?? pracovn??ch uk??zek grafick??ch n??vrh?? (nap??. internetov??ch str??nek, rozvr??en?? ??asopis?? ??i v??ech druh?? reklamn??ch materi??l??). Lipsum tak pracovn?? zn??zor??uje text v uk??zkov??ch maket??ch (tzv. mock-up) p??edt??m, ne?? bude do hotov??ho n??vrhu vlo??en smyslupln?? obsah.\n' +
            '\n' +
            'Pokud by se pro stejn?? ????el pou??il smyslupln?? text, bylo by t????k?? hodnotit pouze vzhled, ani?? by se pozorovatel nechal sv??st ke ??ten?? obsahu. Pokud by byl naopak pou??it nesmysln??, ale pravideln?? text (nap??. opakov??n?? ???asdf asdf asdf??????), oko by p??i posuzov??n?? vzhledu bylo vyru??ov??no pr'
        },
      ],
      // select components
      items:[
        '1.0.0(50)',
      ],
      secondItems:[
        'Copyright 2022 Lorem ipsum s.r.o'
      ],
      firstSelect:null,
      secondSelect:null,

    }
  },
  // Local storage title change
  mounted() {
    this.$store.commit('CHANGE_NAME', {name: 'About us'})
  },
  // Clear selects
  methods: {
    clearForm() { this.firstSelect = this.secondSelect = null }
  }
}

</script>
