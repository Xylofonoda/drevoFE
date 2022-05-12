<template>
  <v-app>
    <v-app-bar app elevation="0">
      <v-img
        src="/Logo-Test.png"
        max-height="100"
        max-width="100"
        contain
        class="mx-auto"
      ></v-img>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>
<script>
export default {
  name: 'HomeLayout',
  data() {
    return {
      miniVariant: false,
    }
  }
}
</script>

