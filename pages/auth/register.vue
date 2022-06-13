<template>
  <v-container fluid class="fill-height">
    <v-row class="text-center" justify="center" align="center" >
      <v-col
        cols="12"
        md="3">
        <v-app-bar fixed app>
          <v-toolbar-title class="ml-2 justify-center">
            <nuxt-link to="/auth/login" style="text-decoration: none"><v-btn fab elevation="0"><v-icon color="#F8B400">mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon></v-btn></nuxt-link>
              Registration Page
          </v-toolbar-title>
        </v-app-bar>
        <v-form>
          <p class="text-center">
            <v-avatar
              width="100px"
              height="100px"
              color="#F8B400">
              <v-icon
              x-large>
                mdi-account
              </v-icon>
            </v-avatar>
          </p>
          <v-text-field
            v-model="firstname"
            :rules="firstnameRules"
            label="First Name"
            persistent-hint
            outlined
            color="white"
            required
          />
          <v-text-field
            v-model="lastname"
            :rules="lastnameRules"
            label="Last Name"
            persistent-hint
            outlined
            color="white"
            required
          />
          <v-text-field
            v-model="email"
            :rules="emailRules"
            label="E-mail"
            color="white"
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
            color="white"
          />
          <v-select
            v-model="countrychoose"
            :rules="countrychooseRules"
            label="Country"
            outlined
            required
            color="white"
            :items="['Česká republika', 'Německo', 'Velká Británie' ]"
          ></v-select>
          <p style="font-weight: 500">Fakturační údaje</p>

          <v-text-field
            v-model="companyname"
            :rules="companynameRules"
            label="Company name"
            persistent-hint
            outlined
            required
            color="white"
          />
          <v-text-field
            v-model="VAT"
            :rules="VATRules"
            label="VAT ID(DIČ)"
            persistent-hint
            outlined
            required
            color="white"
        />
          <v-text-field
            v-model="address"
            :rules="addressRules"
            label="Address"
            persistent-hint
            outlined
            required
            color="white"
        />
          <v-btn
            block
            elevation="3"
            large
            color="#F8B400"
            class="black--text my-4"
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
        v => /^\S+@\S+\.\S+$/.test(v) || "E-mail must be valid"
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
      countrychoose: "",
      countrychooseRules: [
        v => !!v || "Country select is required",
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
