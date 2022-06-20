<template>
  <v-app>
    <v-container class="ml-3 pr-10">
    <v-row>
      <v-col cols="4">
        <thin-card-comp
          title="Registrovaní celkem"
          bignum="3 675"
        ></thin-card-comp>
      </v-col>
      <v-col cols="4">
        <thin-card-comp
          title="uživatelé s min. jednou platbou"
          bignum="3 675"
        ></thin-card-comp>
      </v-col>
      <v-col cols="4">
        <thin-card-comp
          title="Registrovaní celkem"
          bignum="3 675"
        ></thin-card-comp>
      </v-col>
    </v-row>
    </v-container>
  </v-app>
</template>


<script>
export default {
  name: "AdminDatabase",
  layout: "adminlayout",
}
</script>
