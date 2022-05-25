<template>
  <v-app>
    <layout-comp
      title="User Profile"
    ></layout-comp>
    <v-row>
      <v-col
        cols="12"
      ><v-container>
        <p class="text-center"><v-avatar color="black">
          <v-icon dark>
            mdi-account-circle
          </v-icon>
        </v-avatar></p>
        <p class="text-center"><nuxt-link to="/auth/forgotpass" style="color: black"> Change Password</nuxt-link></p>
        <v-form>
          <v-btn
            color="black"
            block
            class="white--text"
          >Logout</v-btn>
          <nuxt-link style="text-decoration: none" to="/app/userprofile"><v-btn
            block
          >Change your credentials</v-btn></nuxt-link>
        </v-form>
      </v-container>

      </v-col>
    </v-row>
  </v-app>
</template>


<script>
  export default {
    name:"UserProfileView",
    layout:"AllroundLayout"
  }
</script>
<style>
 body{
   overflow-y: hidden;
 }
</style>
