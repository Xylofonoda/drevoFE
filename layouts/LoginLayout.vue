<template>
  <v-app dark>
    <v-container class="xs">
      <v-main>
          <Nuxt/>
      </v-main>
      <v-footer color="transparent" bottom absolute padless>
        <span class="mx-auto my-16 pb-6"><nuxt-link to="/app/about" style="color: lightgray; text-decoration: none" >About us</nuxt-link></span>
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
