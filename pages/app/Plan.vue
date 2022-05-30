<template>
  <v-app>
  <layout-comp
    title="Plan"
  ></layout-comp>
  <v-row>
    <v-col>
      <v-container>
        <v-form class="text-center">
          <p>Your Plan:</p>
          <h2
            class="text-h2 text-center"
            style="font-weight: bold"
          >36</h2>
          <p>
            Available evaluations
          </p>
          <p
            style="color: gray"
          >Buy more:</p>
          <plan-card-component
            evals="10 evaluations"
            save="Save 20%"
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
      </v-container>
      <v-btn
        width="100%"
        color="black"
        class="white--text"
      >Buy
      </v-btn>
      <nuxt-link
        to=""
        style="text-decoration: none; color: gray"
      ><p class="text-center subtitle-2 py-3">Proceed to payment gateway</p></nuxt-link>
      <nuxt-link
        to=""
        style="text-decoration-color: black; color: black"
      ><p class="text-center">Historie Plateb (seznam faktur + PDF)</p>
      </nuxt-link>
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
<style scoped>
  html{
    overflow-y: hidden ;
  }
</style>
