<template>
  <v-container fluid class="fill-height">
    <v-row class="text-center" justify="center" align="center" >
      <v-col
        cols="12"
        md="3">
        <v-app-bar fixed app>
          <v-toolbar-title class="ml-2 justify-center">
            <nuxt-link to="/auth/login" style="text-decoration: none"><v-btn elevation="0"><v-icon>mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon></v-btn></nuxt-link>
              Registration Page
          </v-toolbar-title>
        </v-app-bar>
        <v-form>
          <v-img
            contain
            src="/czflag.jpg"
            max-width="100px"
            max-height="100px"
            class="py-16 mx-auto"
          ></v-img>
          <v-text-field
            v-model="firstname"
            :rules="firstnameRules"
            label="First Name"
            persistent-hint
            outlined
            color="black"
            required
          />
          <v-text-field
            v-model="lastname"
            :rules="lastnameRules"
            label="Last Name"
            persistent-hint
            outlined
            color="black"
            required
          />
          <v-text-field
            v-model="email"
            :rules="emailRules"
            label="E-mail"
            outlined
            required
          ></v-text-field>
          <v-text-field
            v-model="password"
            :rules="passwordRules"
            label="Password"
            type="password"
            outlined
            required
            color="black"
          />
          <v-select
            label="Country"
            outlined

          ></v-select>
          <h3>Fakturační údaje</h3>

          <v-text-field
            v-model="companyname"
            :rules="companynameRules"
            label="Company name"
            persistent-hint
            outlined
            required
            color="black"
          />
          <v-text-field
            v-model="VAT"
            :rules="VATRules"
            label="VAT ID(DIČ)"
            persistent-hint
            outlined
            required
            color="black"
        />
          <v-text-field
            v-model="address"
            :rules="addressRules"
            label="Address"
            persistent-hint
            outlined
            required
            color="black"
        />
          <v-btn
            block
            elevation="3"
            large
            color="black"
            class="white--text my-4"
          >Register
          </v-btn>
        </v-form>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name:"RegisterPage",
  layout:"LoginLayout",
  data() {
    return {
      clipped: false,
      miniVariant:false,
      email: "",
      emailRules: [
        v => !!v || "E-mail is required",
        v => /.+@.+/.test(v) || "E-mail must be valid"
      ],
      firstname: "",
      firstnameRules: [
        v => !!v || "First name is required",
      ],

      lastname: "",
      lastnameRules: [
        v => !!v || "Last name is required",
      ],
      password: "",
      passwordRules: [
        v => !!v || "Password is required",
      ],
      companyname: "",
      companynameRules: [
        v => !!v || "Company name is required",
      ],
      VAT: "",
      VATRules: [
        v => !!v || "VAT ID(DIČ) is required",
      ],
      address:"",
      addressRules:[
        v=> !!v || "Adress is required"
      ]




    }
  }
}

</script>
