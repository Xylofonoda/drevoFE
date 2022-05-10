<template>
  <v-container fluid class="fill-height">
    <v-row class="text-center" justify="center" align="center" >
      <v-col
        cols="12"
        md="3">


        <v-app-bar fixed app>
          <v-toolbar-title class="ml-2 justify-center">
            <v-btn elevation="0"><v-icon>mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon></v-btn>
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
            label="First Name"
            persistent-hint
            outlined
            color="black"
          />
          <v-text-field
            label="Last Name"
            persistent-hint
            outlined
            color="black"
          />
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
          <v-select
            :items="items"
            label="Country"
            outlined
            color="black"
          ></v-select>


          <h3>Fakturační údaje</h3>

          <v-text-field
            label="Company name"
            persistent-hint
            outlined
            color="black"
          />
          <v-text-field
            label="VAT ID(DIČ)"
            persistent-hint
            outlined
            color="black"
        />
          <v-text-field
            label="Address"
            persistent-hint
            outlined
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


    }
  }
}

</script>
