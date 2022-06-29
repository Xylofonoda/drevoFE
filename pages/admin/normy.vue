<template>
  <v-app>
    <v-container>
      <v-row>
        <v-col cols="8">
          <thin-card-comp
            title="Název normy"

          >

          </thin-card-comp>
        </v-col>
        <v-col cols="4">
          <thin-card-comp
            title="Časová linka"
          >
          </thin-card-comp>
        </v-col>
      </v-row>
    </v-container>
    <speed-dial>
    </speed-dial>
  </v-app>
</template>

<script>
  export default {
    name:'AdminNormy',
    layout:'adminlayout'
  }
</script>
