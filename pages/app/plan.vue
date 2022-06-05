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
                  class=" text-center"
                  style="font-weight: 600; font-size:60px"
                >36</h2>
                <v-btn
                  x-small
                  fab
                  plain
                  color="#F8B400"
                  style="position: relative; bottom: 80px; left: 50px"
                >
                  <v-icon
                    color="#F8B400"
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
