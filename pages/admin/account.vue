<template>
  <v-app>
    <v-container>
      <v-row>
        <v-col cols="12">
          <v-card
            height="75vh"
            class="rounded-xl"
            color="black"
          >
            <v-card-title class="text-xl-subtitle-1 text-uppercase justify-center font-weight-bold">
              Účet
            </v-card-title>

              <v-row class="justify-center">
                <v-col cols="4" class="ml-xl-3 pb-0 mb-0 ">
                  <v-text-field
                    outlined
                    dense
                    label="Název webové aplikace"
                    :value="nameVal"
                    color="white"
                    clearable
                  ></v-text-field>
                </v-col>
              </v-row>
              <v-row class="justify-center">
                <v-col cols="4" class="ml-xl-3 mt-0 pt-0 mb-0 pb-0">
                  <v-textarea
                    outlined
                    dense
                    :value="descVal"
                    color="white"
                    auto-grow
                    label="Krátký popis společnosti"
                    clearable
                  ></v-textarea>
                </v-col>
              </v-row>
              <v-row class="justify-center">
                <v-col cols="4" class="ml-xl-3 mt-0 pt-0 mb-0 pb-0">
                  <v-text-field
                    outlined
                    dense
                    readonly
                    label="E-mail administrátora"
                    :value="nameVal"
                    color="white"
                  ></v-text-field>
                </v-col>
              </v-row>

            <v-card-actions class="justify-center">
              <v-form
                ref="form"
                v-model="saved"
              >
                <v-btn
                  color="#F8B400"
                  class="ml-xl-2 black--text"
                  @click="save"

                >
                  Uložit
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
    // snackbar Odeslat
    snackbar: false,
    text: 'Vaše připomínka byla zaslána na podporu.',
    timeout: 2000,
    valid: true,
    name: '',
    // snackbar Uložit
    snackbarSave:false,
    textSave:'Úspěšně uloženo',
    saved:true,
    // permanent values
    nameVal: 'Lorem Ipsum',
    descVal: 'Lorem ipsum lorem ipsum  lorem ipsumlorem ipsumlorem ipsumlorem ipsumlorem ipsumlorem ipsum',

    // validation
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
  }),
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
  }
}


</script>
