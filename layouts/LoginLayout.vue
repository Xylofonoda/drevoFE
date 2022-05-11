<template>
  <v-app dark>
    <v-container class="xs">
      <v-main>
          <Nuxt/>
      </v-main>
      <v-footer color="white" app bottom absolute padless>
        <span class="mx-auto "><a href="#" style="color: black">About us</a></span>
      </v-footer>
    </v-container>
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
