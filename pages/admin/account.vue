<template>
  <v-app>
    <v-container>
      <v-row kist>
        <v-col cols="12">
          <v-card
            height="75vh"
            class="rounded-xl"
            color="black"
          >
            <v-card-title class="text-xl-subtitle-1 text-uppercase justify-center font-weight-bold">
              Account settings
            </v-card-title>
            <div class="text-center my-xl-3">
              <v-avatar
                width="100px"
                height="100px"
                color="#F8B400">
                <v-icon
                  x-large>
                  mdi-account
                </v-icon>
              </v-avatar>
            </div>
            <div align="center">
              <v-col cols="6" class="ml-xl-3 pb-0 mb-0 float ">
                <v-row class="justify-center">

                  <v-col cols="4">
                    <v-text-field
                      outlined
                      dense
                      label="Name"
                      :value="nameVal"
                      color="white"
                      clearable
                    ></v-text-field>
                  </v-col>
                  <v-col cols="4">
                    <v-text-field
                      outlined
                      dense
                      label="Surname"
                      :value="nameVal"
                      color="white"
                      clearable
                    ></v-text-field>
                  </v-col>
                </v-row>
              </v-col>
              <v-col cols="4" class="ml-xl-3 mt-0 pt-0 mb-0 pb-0">
                <v-text-field
                  :rules="emailRules"
                  outlined
                  dense
                  :value="emailVal"
                  color="white"
                  auto-grow
                  label="Email"
                  clearable
                ></v-text-field>
              </v-col>
              <v-col cols="4" class="ml-xl-3 mt-0 pt-0 mb-0 pb-0">
                <v-text-field
                  outlined
                  dense
                  :value="nameVal"
                  color="white"
                  auto-grow
                  label="Phone number"
                  clearable
                ></v-text-field>
              </v-col>
              <v-col cols="4" class="ml-xl-3 mt-0 pt-0 mb-0 pb-0">
                <v-text-field
                  v-model="password"
                  outlined
                  dense
                  :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
                  :rules="[rules.required, rules.min]"
                  :type="show1 ? 'text' : 'password'"
                  name="input-10-1"
                  label="Password"
                  hint="State a new password"
                  counter
                  color="white"
                  @click:append="show1 = !show1"

                ></v-text-field>
              </v-col>
              <v-card-actions class="justify-center ">
                <v-form
                  ref="form"
                  v-model="saved"
                >
                  <v-btn
                    color="#F8B400"
                    class="ml-xl-2 black--text"
                    @click="save"

                  >
                    Save
                  </v-btn>
                  <v-snackbar
                    v-model="snackbarSave"
                    color="yellow darken-2"
                    :timeout="timeout"
                    class="rounded-lg"
                    elevation="10"
                  >
                    <div class="text-center black--text pa-0">
                      {{ textSave }}
                    </div>
                  </v-snackbar>
                </v-form>
              </v-card-actions>
            </div>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>
<script>
export default {
  name: 'AdminAccount',
  components: {},
  layout: 'adminlayout',
  data: () => ({
    // snackbar Send
    snackbar: false,
    timeout: 2000,
    valid: true,
    name: '',
    // snackbar Save
    snackbarSave: false,
    textSave: 'Saved successfully',
    saved: true,
    // permanent values
    nameVal: 'Lorem Ipsum',
    descVal: 'Lorem ipsum lorem ipsum  lorem ipsumlorem ipsumlorem ipsumlorem ipsumlorem ipsumlorem ipsum',
    emailVal: 'lorem@ipsum.cz',

    // password input
    show1: false,
    password: 'Password',
    rules: {
      required: value => !!value || 'Required.',
      min: v => v.length >= 8 || 'Min 8 characters',
    },

    // validation
    nameRules: [
      v => !!v || 'Name and surname entries cannot be empty.',
    ],
    emailRules: [
      v => !!v || 'Email entry must not be empty.',
      v => /^\S+@\S+\.\S+$/.test(v) || "E-mail must be valid"
    ],
    phone: '',
    phoneRules: [
      v => !!v || 'Phone number entry must not be empty',
      v => /([+]?\d{1,3}[. \s]?)?(\d{9}?)|([+]?\d{1,3} [.\s]?)?(\d{3}?) (\d{3}?) (\d{3}?)/.test(v) || 'Telefonní číslo musí být platné.'
    ],
  }),
  // Local storage title change
  mounted() {
    this.$store.commit('CHANGE_NAME', {name: 'Account'})
  },
  // button methods
  methods: {
    validate() {
      this.$refs.form.validate()
      this.snackbar = true
      this.$refs.form.reset()
    },
    save() {
      this.snackbarSave = true
    },

  },
}


</script>
