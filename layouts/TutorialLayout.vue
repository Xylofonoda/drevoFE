<template>
  <v-app dark>
    <v-app-bar fixed app>
      <v-toolbar-title
        class="mx-0"
      ><nuxt-link to="/app/home" style="text-decoration: none"><v-btn elevation="0"><v-icon style="float: left" plain>mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon></v-btn></nuxt-link>
        Tutorials
      </v-toolbar-title>
    </v-app-bar>
    <v-container>
      <v-main>
        <Nuxt/>
      </v-main>
    </v-container>
  </v-app>
</template>

<script>

export default {
  name: 'TutorialLayout',
  props:{
    title:{
      type: String,
      default: null,

    }
  },
  data (){
    return{
      fixed:false,
      miniVariant:false,
    }
  }
}

</script>
