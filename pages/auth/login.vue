<template>
  <v-row class="text-center" justify="center" align="center" >
    <v-col
      cols="12"
      md="3">

      <div class="my-2">
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
      </div>

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
            label="ID(E-mail)"
            persistent-hint
            outlined
            color="black"
          />

        <v-text-field
            label="Password"
            persistent-hint
            outlined
            color="black"
          />

        <a href="#" style="color: black">Resend Password</a>

        <v-btn
          block
          elevation="3"
          large
          color="black"
          class="white--text my-5"
        >Login</v-btn>

        <a href="#" style="color: black" class="my-6">Register new account</a>

        <v-footer color="white">
          <a href="#" style="color: black" class="mx-auto pa-15">About us</a>
        </v-footer>

      </v-form>
    </v-col>
  </v-row>
</template>
<script>
export default {
  name: 'LoginPage',
}
</script>
