<template>
  <v-row class="text-center" justify="center">
    <v-col
      cols="12"
      md="3">
      <div class="pa-7 secondary rounded-circle d-inline-block"></div>

      <div></div>
      <v-form class="py-">
        <v-text-field placeholder="ID(E-Mail)" class="py-3"/>
        <v-text-field placeholder="Password" class="py-3"/>
      </v-form>
    </v-col>
  </v-row>
</template>
<script>
export default {
  name: 'LoginPage',
}
</script>
