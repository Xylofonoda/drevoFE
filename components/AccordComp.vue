<template>
  <v-expansion-panels>
    <v-expansion-panel>
      <v-expansion-panel-header class="py-6">
        <v-col cols="2">
          <v-icon
            style="position:absolute; left: 14px; top: 20px"
            size="30px"
            color="black"
          >mdi-square-edit-outline
          </v-icon>
        </v-col>
        {{name}}
      </v-expansion-panel-header>
      <v-expansion-panel-content>
        {{content}}
      </v-expansion-panel-content>
    </v-expansion-panel>
  </v-expansion-panels>
</template>

<script>
export default {
  name: "AccordComp",
  components: {},
  props:{
    name:{
      default:null,
      type:String,
    },
    content:{
      default:null,
      type:String,
    }
  }
}
</script>

