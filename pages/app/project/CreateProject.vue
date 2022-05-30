<template>
  <v-app fluid>
    <layout-component
      title="Vytvořit nový projekt"
    ></layout-component>
    <v-container class="py-8">
      <v-form >
        <v-text-field
          v-model="desc"
          :rules="descRules"
          label="Description"
          persistent-hint
          outlined
          color="black"
          required
        ></v-text-field>
        <v-text-field
          v-model="long"
          :rules="longRules"
          label="Longitude"
          outlined
          color="black"
          required
        ></v-text-field>
        <v-text-field
          v-model="lat"
          :rules="longRules"
          label="Latitude"
          outlined
          color="black"
          required
        ></v-text-field>
        <div>
          <v-menu
            ref="menu"
            v-model="menu"
            :close-on-content-click="false"
            transition="scale-transition"
            offset-y
            min-width="auto"
          >
            <template #activator="{ on, attrs }">
              <v-text-field
                v-model="date"
                :rules="datumRules"
                label="Date"
                color="black"
                readonly
                outlined
                v-bind="attrs"
                required
                v-on="on"
              ></v-text-field>
            </template>
            <v-date-picker
              v-model="date"
              locale="cs-cz"
              color="black"
              :active-picker.sync="activePicker"
              :max="(new Date(Date.now() - (new Date()).getTimezoneOffset() * 60000)).toISOString().substr(0, 10)"
              min="1950-01-01"
              @change="save"
            ></v-date-picker>
          </v-menu>
        </div>
        <v-file-input
          :rules="imgRules"
          accept="image/png, image/jpeg, image/bmp"
          placeholder="Vložte firemní logo"
          prepend-icon="mdi-camera"
          label="Logo"
          color="black"
          outlined
        >
        </v-file-input>
      </v-form>
      <v-btn
        color="black"
        class="white--text"
        block
      >Vytvořit</v-btn>

    </v-container>
  </v-app>
</template>
<script>
  import LayoutComponent from "@/components/LayoutComp";
  export default {
    name:"CreateProject",
    components: {LayoutComponent},
    layout:"ProjectsLayout",
    data: () => ({
      desc:"",
      descRules:[
        v => !!v || "Description must not be empty",
      ],
      long:"",
      longRules:[
        v=> !!v || "Longitude must not be empty"
      ],
      datum:"",
      datumRules:[
        v=> !!v || "Date must not be empty"
      ],
      lat:"",
      latRules:[
        v=> !!v || "Longitude must not be empty"
      ],
      imgRules:[
        value => !value || value.size < 6000000 || 'Avatar size should be less than 6 MB!',
        v=> !!v || "Logo must not be empty"
      ],
      activePicker: null,
      date: null,
      menu: false,
    }),
    watch: {
      menu (val) {
        val && setTimeout(() => (this.activePicker = 'YEAR'))
      },
    },
    methods: {
      save (date) {
        this.$refs.menu.save(date)
      },
    },
  }
</script>
<style scoped>
  html{
    overflow-y: hidden
  }
</style>
