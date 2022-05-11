<template>
  <v-row class="text-center" justify="center" align="center" >
    <v-col
      cols="12"
      md="3">
        <v-app-bar fixed app elevation="0">
          <v-toolbar-title class="ml-2 justify-center">
            <nuxt-link to="/auth/login" style="text-decoration: none"><v-btn elevation="0"><v-icon>mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon></v-btn></nuxt-link>
            Password Recovery
          </v-toolbar-title>
        </v-app-bar>
      <v-container style="padding-top: 120px">
        <v-card class="py-8 px-4">
          <v-form>
            <p style="text-align: left">Zvolte nové heslo:</p>
            <v-text-field
              v-model="password"
              :rules="passwordRules"
              label="Password"
              type="password"
              required
              outlined
          ></v-text-field>
            <p style="text-align: left">Potvrďte nové heslo:</p>
            <v-text-field
              v-model="confirmPassword"
              :rules="confirmPasswordRules.concat(passwordConfirmationRule)"
              label="Confirm Password"
              type="password"
              required
              outlined
          ></v-text-field>
            <div class="d-flex justify-space-between text-caption">
              <div>
                <div class="grey--text mb-2">
                  Hesla se musí shodovat.
                </div>
              </div>
            </div>
            <v-btn
              block
              elevation="3"
              large
              color="black"
              class="white--text my-4"
            >Potvrdit</v-btn>
          </v-form>
        </v-card>
      </v-container>
    </v-col>
  </v-row>
</template>
<script>
export default {
  name: 'PassRec',
  layout:"LoginLayout",

  data: () => ({
    valid: true,
    password: "",
    confirmPassword: "",
    passwordRules: [v => !!v || "Password is required"],
    confirmPasswordRules: [v => !!v || "Password is required"]
  }),

  computed: {
    passwordConfirmationRule() {
      return () =>
        this.password === this.confirmPassword || "Password must match";
    }
  }
}
</script>
