<template>
  <v-app>
    <v-container>
      <v-row>
        <v-col cols="8">
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
                <v-card-subtitle class="pa-0 ma-0 ml-4">
                  TYP
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
                </v-tabs-items>

              </v-col>
            </v-row>
          </v-card>
        </v-col>
        <v-col cols="4">
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
                  color="pink"
                  small
                >
                  <v-row class="pt-1">
                    <v-col cols="3">
                      <strong>5pm</strong>
                    </v-col>
                    <v-col>
                      <strong>New Icon</strong>
                      <div class="text-caption">
                        Mobile App
                      </div>
                    </v-col>
                  </v-row>
                </v-timeline-item>

                <v-timeline-item
                  color="teal lighten-3"
                  small
                >
                  <v-row class="pt-1">
                    <v-col cols="3">
                      <strong>3-4pm</strong>
                    </v-col>
                    <v-col>
                      <strong>Design Stand Up</strong>
                      <div class="text-caption mb-2">
                        Hangouts
                      </div>
                      <v-avatar>
                        <v-img
                          src="https://avataaars.io/?avatarStyle=Circle&topType=LongHairFrida&accessoriesType=Kurt&hairColor=Red&facialHairType=BeardLight&facialHairColor=BrownDark&clotheType=GraphicShirt&clotheColor=Gray01&graphicType=Skull&eyeType=Wink&eyebrowType=RaisedExcitedNatural&mouthType=Disbelief&skinColor=Brown"
                        ></v-img>
                      </v-avatar>
                      <v-avatar>
                        <v-img
                          src="https://avataaars.io/?avatarStyle=Circle&topType=ShortHairFrizzle&accessoriesType=Prescription02&hairColor=Black&facialHairType=MoustacheMagnum&facialHairColor=BrownDark&clotheType=BlazerSweater&clotheColor=Black&eyeType=Default&eyebrowType=FlatNatural&mouthType=Default&skinColor=Tanned"
                        ></v-img>
                      </v-avatar>
                      <v-avatar>
                        <v-img
                          src="https://avataaars.io/?avatarStyle=Circle&topType=LongHairMiaWallace&accessoriesType=Sunglasses&hairColor=BlondeGolden&facialHairType=Blank&clotheType=BlazerSweater&eyeType=Surprised&eyebrowType=RaisedExcited&mouthType=Smile&skinColor=Pale"
                        ></v-img>
                      </v-avatar>
                    </v-col>
                  </v-row>
                </v-timeline-item>

                <v-timeline-item
                  color="pink"
                  small
                >
                  <v-row class="pt-1">
                    <v-col cols="3">
                      <strong>12pm</strong>
                    </v-col>
                    <v-col>
                      <strong>Lunch break</strong>
                    </v-col>
                  </v-row>
                </v-timeline-item>

                <v-timeline-item
                  color="teal lighten-3"
                  small
                >
                  <v-row class="pt-1">
                    <v-col cols="3">
                      <strong>9-11am</strong>
                    </v-col>
                    <v-col>
                      <strong>Finish Home Screen</strong>
                      <div class="text-caption">
                        Web App
                      </div>
                    </v-col>
                  </v-row>
                </v-timeline-item>
              </v-timeline>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
    <speed-dial>
    </speed-dial>
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
        {
          title: 'detail',
        },
        {
          title: 'informace'
        }
      ],
    }
  },
}
</script>
