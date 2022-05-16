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

          <v-list>
            <v-list-item-group
              v-model="model"
            >
              <template v-for="(item, i) in items">

                <v-divider
                  v-if="!item"
                  :key="`divider-${i}`"
                ></v-divider>

                <v-list-item
                  v-else
                  :key="`item-${i}`"
                  :value="item"
                  active-class="black--text"
                >
                  <template #default="{ active }">
                    <v-list-item-action>
                      <v-checkbox
                        :input-value="active"
                        color="black"
                      ></v-checkbox>
                    </v-list-item-action>
                    <v-list-item-content>
                      <v-list-item-title
                        align="left"
                        v-text="item"
                      ></v-list-item-title>
                    </v-list-item-content>
                    <v-list-item-action>
                    </v-list-item-action>
                  </template>
                </v-list-item>
              </template>
            </v-list-item-group>
          </v-list>
        </v-form>
      </v-container>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "PlanPage",
  data: () => ({
    items: [
      '10 evaluations',
      '50 evaluation',
      '200 evaluations',
    ],
    model: [''],
  }),
}
</script>
