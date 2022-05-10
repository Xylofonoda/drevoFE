<template>
  <v-app dark>
    <v-main>
        <Nuxt />
    </v-main>

    <v-footer color="white">
      <span class="mx-auto "><a href="#" style="color: black">About us</a></span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'LoginLayout',
  data (){
    return{
      fixed:false
    }
  }
}
</script>
