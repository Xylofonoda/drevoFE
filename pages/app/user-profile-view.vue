<template>
  <v-app>
    <layout-comp
      title="User Profile"
      :items="[
      { name: 'Přejmenovat' },
      { name: 'Smazat' },
    ]"
    ></layout-comp>
    <v-row class="ma-0">
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
          <v-form class="pt-2">
            <v-btn
              color="#F8B400"
              block
              class="black--text"
            >Logout
            </v-btn>
            <p class="text-center pt-2">
              <nuxt-link to="/auth/forgotpass" style="color: white; text-decoration: none"> Change Password</nuxt-link>
            </p>
            <nuxt-link to="/app/user-profile" style="color: white; text-decoration: none">
              <p class="text-center ">
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
