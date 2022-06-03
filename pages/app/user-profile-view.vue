<template>
  <v-app>
    <layout-comp
      title="User Profile"
    ></layout-comp>
    <v-row>
      <v-col
        cols="12"
      >
        <v-container>
          <p class="text-center">
            <v-avatar color="#F8B400">
              <v-icon>
                mdi-account
              </v-icon>
            </v-avatar>
          </p>
          <p class="text-center">
            <nuxt-link to="/auth/forgotpass" style="color: white"> Change Password</nuxt-link>
          </p>
          <v-form class="pt-2">
            <v-btn
              color="black"
              block
              class="white--text"
            >Logout
            </v-btn>
            <nuxt-link to="/app/user-profile" style="color: white">
              <p class="text-center pt-3">
                Change your credentials
              </p>
            </nuxt-link>
          </v-form>
        </v-container>
      </v-col>
    </v-row>
  </v-app>
</template>


<script>
export default {
  name: "UserProfileView",
  layout: "AllroundLayout"
}
</script>
<style scoped>
body {
  overflow-y: hidden;
}
</style>
