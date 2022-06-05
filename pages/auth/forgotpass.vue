<template>
  <v-row class="text-center" justify="center" align="center" >
    <v-col
      cols="12"
      md="3">
        <v-app-bar fixed app elevation="0">
          <v-toolbar-title class="ml-2 justify-center">
            <nuxt-link to="/auth/login" style="text-decoration: none"><v-btn elevation="0"><v-icon fab color="#F8B400">mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon></v-btn></nuxt-link>
            Password Recovery
          </v-toolbar-title>
        </v-app-bar>
      <v-container style="padding-top: 120px">
        <v-card class="py-8 px-4">
          <v-form>
            <p style="text-align: left">Email:</p>
            <v-text-field
              v-model="email"
              :rules="emailRules"
              label="E-mail"
              outlined
              required
              dark
              color="white"
          ></v-text-field>
            <div class="d-flex justify-space-between text-caption">
              <div>
                <div class="grey--text mb-2">
                  Použijte email který jste použil/a u registrace.
                </div>
              </div>
            </div>
            <v-btn
              block
              elevation="3"
              large
              color="#F8B400"
              class="black--text my-4"
            >Potvrdit</v-btn>
          </v-form>
        </v-card>
      </v-container>
    </v-col>
  </v-row>
</template>
<script>
export default {
  name: 'ForgotPass',
  layout:"LoginLayout",

  data: () => ({
    valid: true,
      email: "",
      emailRules: [
        v => !!v || "E-mail is required",
        v => /.+@.+/.test(v) || "E-mail must be valid"
      ],

    }
  )

}
</script>
