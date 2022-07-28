<template>
  <v-app>
    <v-container>
      <v-row>
        <v-col cols="12" sm="12" xl="8" md="8">
          <v-card
            height="75vh"
            class="rounded-xl"
            color="black"
          >
            <v-card-title class="text-xl-subtitle-1 font-weight-bold text-uppercase white--text black">
              Název normy
            </v-card-title>
            <v-row no-gutters>
              <v-col cols="12">
                <v-card-subtitle class="pa-0 ma-0 ml-4 text-uppercase">
                  typ
                </v-card-subtitle>
                <v-card-title class="pa-0 ma-0 ml-4 text-xl-h4 font-weight-bold">Hodnota (50mm)</v-card-title>
                <v-card-subtitle class="pt-4">#01623 Jméno Příjmení</v-card-subtitle>
                <v-divider></v-divider>
                  <v-tabs
                    v-model="tab"
                    background-color="black"
                    class="my-xl-5"
                  >
                    <v-tabs-slider color="white"></v-tabs-slider>
                    <v-tab
                      v-for="item in items"
                      :key="item.title"
                      style="color: white"
                    >
                      {{ item.title }}
                    </v-tab>
                  </v-tabs>

                <v-tabs-items v-model="tab">
                  <v-tab-item>
                    <v-card
                    color="black"
                    >
                      <v-row no-gutters>
                        <v-card-subtitle style="color:gray;" class="pa-0 ma-0 ml-4">Hodnota v mm</v-card-subtitle>
                      </v-row>
                      <v-card-text style="max-width: 300px">
                        <v-text-field
                          class="ma-0 pa-0"
                          color="white"
                          suffix="mm"
                        ></v-text-field>
                      </v-card-text>
                      <v-col cols="4">
                        <v-card-actions class="pl-16 ml-15 ma-0 pa-0">
                          <v-btn
                            color="white"
                            text
                            class="pt-0"
                          >
                            Zrušit
                          </v-btn>
                          <v-btn
                            color="#F8B400"
                            text
                          >
                            Uložit
                          </v-btn>
                        </v-card-actions>
                      </v-col>
                    </v-card>
                  </v-tab-item>
                  <v-tab-item>
                    <v-card
                      color="black"
                    >
                      <v-row no-gutters>
                        <v-card-subtitle style="color:gray;" class="pa-0 ma-0 ml-4">Hodnota </v-card-subtitle>
                      </v-row>
                      <v-card-text style="max-width: 300px">
                        <v-text-field
                          class="ma-0 pa-0"
                          color="white"
                          suffix="mm"
                        ></v-text-field>
                      </v-card-text>
                      <v-col cols="4">
                        <v-card-actions class="pl-16 ml-15 ma-0 pa-0">
                          <v-btn
                            color="white"
                            text
                            class="pt-0"
                          >
                            Zrušit
                          </v-btn>
                          <v-btn
                            color="#F8B400"
                            text
                          >
                            Uložit
                          </v-btn>
                        </v-card-actions>
                      </v-col>
                    </v-card>
                  </v-tab-item>
                </v-tabs-items>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
        <v-col cols="12" xl="4" md="4" sm="12">
          <v-card
            height="100%"
            class="rounded-xl"
            color="black"
          >
            <v-card-title class="text-xl-subtitle-1 font-weight-bold text-uppercase white--text black">
              časová linka
            </v-card-title>
            <v-card-text class="py-0">
              <v-timeline
                align-top
                dense
              >
                <v-timeline-item
                  v-for="item in timeline"
                  :key="item.time"
                  color="#F8B400"
                  small
                >
                  <v-row>
                    <v-col cols="4">
                      <strong>{{item.nameTask}}</strong>
                      <div class="text-caption">
                        {{item.taskDesc}}
                      </div>
                    </v-col>
                    <v-col >
                      <strong>{{item.time}}</strong>
                    </v-col>
                  </v-row>
                </v-timeline-item>
              </v-timeline>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>

  </v-app>
</template>

<script>
export default {
  name: 'AdminNormy',
  layout: 'adminlayout',
  data () {
    return {
      tab: null,
      items: [
        // Input navigation
        {
          title: 'detail',
        },
        {
          title: 'informace'
        }
      ],
      // Timeline component content
      timeline:[
        {
          time:'2.11 2021',
          nameTask:'LoremeIpsum',
          taskDesc:'Lorem Ipsum'
        },
        {
          time:'3.11 2021',
          nameTask:'LoremeeIpsum',
          taskDesc:'Lorems Ipsum'
        },
        {
          time:'4.11 2021',
          nameTask:'LoremasIpsum',
          taskDesc:'Loremd Ipsum'
        },
        {
          time:'5.11 2021',
          nameTask:'LoremssIpsum',
          taskDesc:'Lorem4 Ipsum'
        },
        {
          time:'6.11 2021',
          nameTask:'LoremasasdIpsum',
          taskDesc:'Loreaasdm Ipsum'
        },

      ]
    }
  },
}
</script>
