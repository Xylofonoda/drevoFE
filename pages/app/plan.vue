<template>
  <v-app>
    <layout-comp
      title="Plan"
    ></layout-comp>
    <v-row>
      <v-col>
        <v-container class="justify-center">
          <v-form class="text-center">
            <p style="font-size: small">Your Plan:</p>
            <v-row>
              <v-col cols="12">
                <h2
                  class="text-h2 text-center"
                  style="font-weight: bold;"
                >36</h2>
                <v-btn
                  x-small
                  fab
                  plain
                  color="black"
                  style="position: relative; bottom: 60px; left: 50px"
                >
                  <v-icon
                    color="black"
                  >mdi-help-circle-outline
                  </v-icon>
                </v-btn>
              </v-col>
            </v-row>
            <p>
              Available evaluations
            </p>
            <p
              style="color: gray"
            >Buy more:</p>
            <plan-card-component
              evals="10 evaluations"
              price="1500 Kč"
            ></plan-card-component>
            <plan-card-component
              evals="30 evaluations"
              save="Save 20%"
              price="7000 Kč"
            ></plan-card-component>
            <plan-card-component
              evals="50 evaluations"
              save="Save 20%"
              price="21000 Kč"
            ></plan-card-component>
          </v-form>
          <v-btn
            width="100%"
            color="black"
            class="white--text my-5"
          >Buy
          </v-btn>
          <nuxt-link
            to=""
            style="text-decoration: none; color: gray"
          ><p class="text-center subtitle-2 py-3">Proceed to payment gateway</p></nuxt-link>
          <nuxt-link
            to=""
            style="text-decoration-color: black; color: black"
          ><p class="text-center mb-10">Historie Plateb (seznam faktur + PDF)</p>
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

}
</script>
