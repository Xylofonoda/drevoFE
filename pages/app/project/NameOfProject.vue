<template>
  <v-app>
    <layout-comp
      title="Trám 2B"
    ></layout-comp>
    <accord-comp
    name="Subproject description"
    >
    </accord-comp>
    <folders-comp>
    </folders-comp>

    <p class="text-center">
      <v-btn
        outlined
        fab
        max-width="50px"
        max-height="50px"
        style="bottom: 260px"
        to="/app/project/addmeasurement"
      >
        <v-icon
          size="50px"
        >mdi-plus
        </v-icon>

      </v-btn>
    </p>
  </v-app>
</template>

<script>
  export default {
    name:"NameOfProject",
    layout:"AllroundLayout"
  }
</script>
<style>
  html{
    overflow-y: hidden;
  }
</style>
