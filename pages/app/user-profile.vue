<template>
  <v-app>
    <layout-comp
      title="Change"
    ></layout-comp>
    <v-container fluid class="fill-height">
      <v-row class="text-center" justify="center" align="center" >
        <v-col
          cols="12"
          md="3">
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
              outlined
              color="white"
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
              color="#F8B400"
              class="black--text"
            >
              Save Changes
            </v-btn>
          </v-form>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
export default {
  name:"UserProfile",
  layout:"AllroundLayout",
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
<style scoped>
  body{
    overflow-y: auto;
  }
</style>
