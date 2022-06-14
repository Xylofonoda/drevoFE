<template>
  <v-app>
    <layout-comp
      title="Plan"
      :items="[
      { name: 'Přejmenovat' },
      { name: 'Smazat' },
    ]"
    ></layout-comp>
    <v-row class="ma-0">
      <v-col>
        <v-container class="justify-center">
          <v-form class="text-center">
            <p style="font-size: small">Your Plan:</p>
            <v-row>
              <v-col cols="12">
                <h2
                  class=" text-center"
                  style="font-weight: 600; font-size:60px"
                >36</h2>
                <v-dialog
                  v-model="planquest"
                  width="300"
                >
                  <template #activator="{ on, attrs }">
                    <v-btn
                      v-bind="attrs"
                      x-small
                      fab
                      plain
                      color="#F8B400"
                      style="position: relative; bottom: 80px; left: 50px"
                      v-on="on"
                    >
                      <v-icon
                        color="#F8B400"
                      >mdi-help-circle-outline
                      </v-icon>
                    </v-btn>
                  </template>
                  <v-card>
                    <v-card-title class="text-h5 black--text amber darken-1">
                      Available evaluations
                    </v-card-title>
                    <v-card-text class="pt-2">
                      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
                      labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris
                      nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit
                      esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt
                      in culpa qui officia deserunt mollit anim id est laborum.
                    </v-card-text>
                    <v-divider></v-divider>
                    <v-card-actions>
                      <v-spacer></v-spacer>
                      <v-btn
                        class="white--text"
                        text
                        @click="planquest = false"
                      >
                        OK
                      </v-btn>
                    </v-card-actions>
                  </v-card>
                </v-dialog>
              </v-col>
            </v-row>
            <p>
              Available evaluations
            </p>
            <p
              style="color: gray"
            >Buy more:</p>
            <v-item-group>
              <v-item>
                <plan-card-component
                  evals="10 evaluations"
                  price="1500 Kč"
                ></plan-card-component>
              </v-item>
              <v-item>
                <plan-card-component
                  evals="30 evaluations"
                  save="Save 20%"
                  price="7000 Kč"
                ></plan-card-component>
              </v-item>
              <v-item>
                <plan-card-component
                  evals="50 evaluations"
                  save="Save 20%"
                  price="21000 Kč"
                ></plan-card-component>
              </v-item>
            </v-item-group>
          </v-form>
          <v-btn
            width="100%"
            color="#F8B400"
            class="black--text my-5"
          >Buy
          </v-btn>
          <nuxt-link
            to=""
            style="text-decoration: none; color: gray"
          ><p class="text-center subtitle-2 py-3">Proceed to payment gateway</p></nuxt-link>
          <nuxt-link
            to=""
            style="text-decoration:none; color: #F8B400"
          ><p class="text-center mb-6">Historie Plateb (seznam faktur + PDF)</p>
          </nuxt-link>
        </v-container>
      </v-col>
    </v-row>
  </v-app>
</template>

<script>
import PlanCardComponent from "@/components/PlanCard";

export default {
  name: "PlanPage",
  components: {PlanCardComponent},
  layout: "AllroundLayout",
  data() {
    return {
      planquest: false,
    }
  },

}
</script>
