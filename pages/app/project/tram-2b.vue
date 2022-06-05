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
          Trám 2B
        </v-expansion-panel-header>
        <v-expansion-panel-content class="pt-6">
          <v-row class="justify-end align-center" justify="flex-end">
            <v-row>
              <v-col cols="10">
                <p
                  style="color: gray"
                >Rozměry v prvku (mm):</p>
              </v-col>
              <v-col cols="2">
                <v-btn
                  elevation="0"
                  plain
                  fab
                  color="white"
                >
                  <v-icon
                    color="#F8B400"
                  >mdi-help-circle-outline
                  </v-icon>
                </v-btn>
              </v-col>
            <v-col cols="6" align-self="end">
              <v-img
                src="/sirka.png"
                max-height="70px"
                max-width="90px"
                class="mx-auto"
              ></v-img>
              <v-text-field
                outlined
                label="Šířka (b)"
                color="white"
                class="pt-2"
              ></v-text-field>
            </v-col>
            <v-col cols="6" align-self="end">
              <v-img
                src="/vyska1.png"
                class="mx-auto"
                max-height="103px"
                max-width="60px"
              ></v-img>
              <v-text-field
                outlined
                label="Výška (d)"
                color="white"
                class="pt-2"
              ></v-text-field>
            </v-col>
            </v-row>

          </v-row>
          <v-divider></v-divider>
          <v-row class="pt-3">
            <v-col cols="7">
              <p style="color: gray;">Orientace prvku:</p>
            </v-col>
            <v-col cols="6">
              <v-col cols="12">
                <v-img
                  src="/orientaceprvku1.png"
                  class="mx-auto"
                  max-height="70px"
                  max-width="90px"

                ></v-img>
              </v-col>
              <v-row justify="center">
                    <v-checkbox
                      color="#F8B400"
                    ></v-checkbox>
              </v-row>
            </v-col>
            <v-col cols="6">
              <v-col cols="12">
                <v-img
                  src="/orientaceprvku2.png"
                  class="mx-auto"
                  max-height="120px"
                  max-width="65px"
                ></v-img>
              </v-col>
              <v-row justify="center">
                <v-checkbox
                  color="#F8B400"

                ></v-checkbox>
              </v-row>

            </v-col>
          </v-row>
          <v-divider></v-divider>
          <v-row class="pt-3">
            <v-col cols="10">
              <p

                style="color: gray"
              >Suky:</p>
            </v-col>
            <v-col cols="2">
              <v-btn
                elevation="0"
                plain
                fab
                style="bottom: 17px"
                color="white"
              >
                <v-icon
                  color="#F8B400"
                >mdi-help-circle-outline
                </v-icon>
              </v-btn>
            </v-col>
            <v-col cols="4">
              <v-col cols="12">
                <v-img
                  src="/suk1.png"
                  class="mx-auto pr-1"
                  max-width="60px"
                  max-height="80px"
                ></v-img>
              </v-col>
              <v-row justify="center">
                <v-checkbox
                  color="#F8B400"
                ></v-checkbox>
              </v-row>
            </v-col>
            <v-col cols="4">
              <v-col cols="12">
                <v-img
                  src="/suk2.png"
                  class="mx-auto pr-0"
                  max-width="60px"
                  max-height="80px"
                ></v-img>
              </v-col>
            <v-row justify="center">
              <v-checkbox
                color="#F8B400"
              ></v-checkbox>
            </v-row>
            </v-col>
            <v-col cols="4">
              <v-col cols="12">
                <v-img
                  src="/suk3.png"
                  class="mx-auto pr-0"
                  max-width="60px"
                  max-height="80px"
                ></v-img>
              </v-col>
             <v-row justify="center">
               <v-checkbox
                 color="#F8B400"
               ></v-checkbox>
             </v-row>

            </v-col>
          </v-row>
          <v-divider></v-divider>
          <v-row class="pt-3">
            <v-col cols="10">
              <p style="color: gray">Odklon vláken:</p>
            </v-col>
            <v-col cols="2">
              <v-btn
                plain
                fab
                style="bottom: 17px"
                color="white"
              >
                <v-icon
                  color="#F8B400"
                >mdi-help-circle-outline
                </v-icon>
              </v-btn>
            </v-col>
            <v-col cols="4">
              <v-col cols="12">
                <v-img
                  src="/odklon1.png"
                  class="mx-auto pr-1"
                  max-width="60px"
                  max-height="80px"
                ></v-img>
              </v-col>
              <v-row justify="center">
                <v-checkbox
                  color="#F8B400"
                ></v-checkbox>
              </v-row>
            </v-col>
            <v-col cols="4">
              <v-col cols="12">
                <v-img
                  src="/odklon2.png"
                  class="mx-auto pr-1"
                  max-width="60px"
                  max-height="80px"
                ></v-img>
              </v-col>
              <v-row justify="center" class="pt-1">
                <v-checkbox
                  color="#F8B400"
                ></v-checkbox>
              </v-row>
            </v-col>
            <v-col cols="4">
              <v-col cols="12">
                <v-img
                  src="/odklon3.png"
                  class="mx-auto pr-1"
                  max-width="60px"
                  max-height="80px"
                ></v-img>
              </v-col>
              <v-row justify="center">
                <v-checkbox
                  color="#F8B400"
                ></v-checkbox>
              </v-row>
            </v-col>
          </v-row>
            <v-divider></v-divider>
            <v-row class="pt-3">
              <v-col cols="10">
                <p style="color: gray">Typ dřeva:</p>
              </v-col>
              <v-col cols="2">
                <v-btn
                  plain
                  fab
                  style="bottom: 17px"
                  color="white"
                >
                  <v-icon
                    color="#F8B400"
                  >mdi-help-circle-outline
                  </v-icon>
                </v-btn>
              </v-col>
              <v-col cols="12">
                <v-card elevation="0">
                  <v-select
                    label="Typ dřeva"
                    outlined
                    color="white"
                  ></v-select>
                  <v-select
                    label="Původ dřeva"
                    outlined
                    color="white"
                  ></v-select>
                  <v-textarea
                    outlined
                    label="Popis prvku(nepovinné)"
                    color="white"
                  >
                  </v-textarea>
                  <v-btn
                    block
                    color="#F8B400"
                    class="black--text mb-16"
                  >Save Description</v-btn>
                </v-card>
              </v-col>
            </v-row>
        </v-expansion-panel-content>
      </v-expansion-panel>
    </v-expansion-panels>
  </v-app>
</template>

<script>
export default {
  name: "Tram2BPage",
  layout: "AllroundLayout"
}
</script>

