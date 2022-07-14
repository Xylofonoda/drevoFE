<template>
  <v-app>
    <v-container>
      <v-row>
        <v-col cols="6">
          <v-card
            height="75vh"
            class="rounded-xl"
            color="black"
          >
            <v-card-title class="text-xl-subtitle-1 text-uppercase font-weight-bold">
              Základní nastavení
            </v-card-title>

          </v-card>
        </v-col>
        <v-col cols="6">
          <v-card
            height="100%"
            class="rounded-xl"
            color="black"
          >
              <v-card-title class="text-xl-subtitle-1 text-uppercase font-weight-bold">
                  Kontaktní formulář na podporu
              </v-card-title>
            <v-container>
              <v-form
                ref="form"
                v-model="valid"
                lazy-validation
              >
                <v-text-field
                  v-model="name"
                  :rules="nameRules"
                  label="Jméno a přijmení"
                  color="white"
                  outlined
                  dense
                  required
                  clearable
                ></v-text-field>
                <v-text-field
                  v-model="email"
                  :rules="emailRules"
                  label="E-mail"
                  color="white"
                  outlined
                  dense
                  required
                  clearable
                ></v-text-field>
                <v-text-field
                  v-model="phone"
                  :rules="phoneRules"
                  label="Telefonní číslo"
                  color="white"
                  outlined
                  dense
                  required
                  hint="Use a number with your country prefix eg. +420, +91"
                  clearable
                ></v-text-field>
                <v-textarea
                  v-model="textArea"
                  class="pt-xl-1"
                  outlined
                  label="Popis problému"
                  auto-grow
                  :rules="textAreaRules"
                  color="white"
                  clearable
                ></v-textarea>


                <v-btn
                  :disabled="!valid"
                  color="#F8B400"
                  class="mr-4 black--text"
                  @click="validate"
                >
                  Odeslat
                </v-btn>
                <v-snackbar
                  v-model="snackbar"
                  color="yellow darken-2"
                  :timeout="timeout"
                  class="rounded-lg"
                  elevation="10"
                >
                 <div class="text-center black--text pa-0">
                   {{ text }}
                 </div>
                </v-snackbar>


              </v-form>
            </v-container>

          </v-card>
        </v-col>
      </v-row>

    </v-container>
  </v-app>
</template>
<script>
export default {
  name: 'AdminSettings',
  components:{},
  layout: 'adminlayout',
  data: () => ({
    snackbar: false,
    text: 'Vaše připomínka byla zaslána na podporu.',
    timeout: 2000,
    valid: true,
    name: '',
    nameRules: [
      v => !!v || 'Pole Jména a příjmení nesmí být prázdné',

    ],
    email: '',
    emailRules: [
      v => !!v || 'Pole e-mailu nesmí být prázdné',
      v => /^\S+@\S+\.\S+$/.test(v) || "E-mail must be valid"
    ],
    textArea: '',
    textAreaRules: [
      v => !!v || 'Pole nesmí být prázdné',
    ],
    phone: '',
    phoneRules: [
      v => !!v || 'Pole nesmí být prázdné',
      v => /([+]?\d{1,3}[. \s]?)?(\d{9}?)|([+]?\d{1,3} [.\s]?)?(\d{3}?) (\d{3}?) (\d{3}?)/.test(v) || 'Telefonní číslo musí být platné.'
    ],

    checkbox: false,
  }),
  methods: {
    validate() {
      this.$refs.form.validate()
      this.snackbar = true
      this.$refs.form.reset()
    },
  }
}


</script>
