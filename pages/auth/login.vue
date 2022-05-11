<template>
  <v-row class="text-center" justify="center" align="center" >
    <v-col
      cols="12"
      md="3">

        <v-btn
          dark
          fab
        >
          <v-img
            contain
            src="/czflag.jpg"
            max-width="50px"
            max-height="50px"
            class="px-1 py-1"
          ></v-img>
        </v-btn>
        <v-btn
          fab
        >
          <v-img
            contain
            src="/UKflag.jpg"
            max-width="50px"
            max-height="50px"
            class="px-1 py-1"
          ></v-img>
        </v-btn>
        <v-btn
          fab
        >
          <v-img
            contain
            src="/germanflag.jpg"
            max-width="50px"
            max-height="50px"
            class="px-1 py-1"
          ></v-img>
        </v-btn>
      <v-form>

        <v-img
          contain
          lazy-src="https://picsum.photos/id/11/10/6"
          max-height="300"
          max-width="200"
          class="py-3 mx-auto"
          src="https://picsum.photos/id/11/500/300"
        ></v-img>
          <v-text-field
            v-model="email"
            :rules="emailRules"
            label="ID(E-mail)"
            persistent-hint
            outlined
            color="black"
          />
        <v-text-field
            v-model="password"
            :rules="passwordRules"
            label="Password"
            persistent-hint
            type="password"
            outlined
            color="black"
          />

        <nuxt-link to="/auth/passRec" style="color: black">Resend Password</nuxt-link>
        <v-btn
          block
          elevation="3"
          large
          color="black"
          class="white--text my-4"
        >Login</v-btn>
        <nuxt-link to="/auth/register" style="color: black" class="my-6">Register new account</nuxt-link>
        </v-form>

    </v-col>
  </v-row>
</template>
<script>
export default {
  name: 'LoginPage',
  layout:"LoginLayout",
  data() {
    return {
      email: "",
      emailRules: [
        v => !!v || "ID(E-mail) is required",
        v => /.+@.+/.test(v) || "E-mail must be valid"
      ],
      password: "",
      passwordRules: [
        v => !!v || "Password is required",
      ],
    }
  }
}
</script>
