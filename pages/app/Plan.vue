<template>
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
            v-model="checkboxOnce"
            evals="10 evaluations"
            save="Save 20%"
          ></plan-card-component>
          <plan-card-component
            v-model="checkboxOnce"
            evals="30 evaluations"
            save="Save 20%"
          ></plan-card-component>
          <plan-card-component
            v-model="checkboxOnce"
            evals="50 evaluations"
            save="Save 20%"
          ></plan-card-component>
        </v-form>
      </v-container>
    </v-col>
  </v-row>
</template>

<script>
import PlanCardComponent from "@/components/PlanCard";

export default {
  name: "PlanPage",
  components: {PlanCardComponent},

}
</script>
