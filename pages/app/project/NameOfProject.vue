<template>
  <v-app>
    <layout-comp
      title="Trám 2B"
    ></layout-comp>

    <accord-comp
      name="Subproject description"
    >
    </accord-comp>
    <folders-comp
    ></folders-comp>
    <v-row justify="center">
      <v-btn
        outlined
        fab
        to="/app/project/tram2b"
        fixed
        class="mb-7"
        bottom
      >
        <v-icon
          size="50px"
        >mdi-plus
        </v-icon>
      </v-btn>
    </v-row>
  </v-app>
</template>

<script>
  export default {
    name:"NameOfProject",
    layout:"AllroundLayout"
  }
</script>

