<template>
  <v-app>
    <v-container class="ml-3 pr-10">
      <v-row>
        <v-col
          v-for="item in cards"
          :key="item.cardtitle"
          cols="12"
          xl="4"
          md="4"
          sm="12">
          <thin-card-comp
            :title="item.cardtitle"
            :bignum="item.bignum"
            :styling="item.styling"
            :icon="item.icon"
            :icon-right="item.iconRight"
          ></thin-card-comp>
        </v-col>
        <v-col cols="12" xl="4" md="4" sm="12">
          <v-card
            class="rounded-xl"
            outlined
            color="gray"
            rounded
            link
          >
            <p class="text-center my-16">
              <v-btn
                outlined
                fab
                disabled

              >
                <v-icon
                  size="50px"
                  class="mx-auto"
                >mdi-plus
                </v-icon>
              </v-btn>
            </p>
          </v-card>
        </v-col>
      </v-row>
      <v-row class="pt-xl-5 pt-md-3">
        <v-col cols="4">
          <p class="text-start text-uppercase text-xl-h6 mt-xl-3" style="font-weight: 600">
            registrovaní uživatelé
          </p>
        </v-col>
        <v-col cols="4">
          <v-card
            outlined
            color="gray"
          >
            <v-row>
              <v-col cols="12">
                <v-text-field
                  v-model="search"
                  class="px-4 my-0 text-uppercase"
                  label="hledat"
                  append-icon="mdi-magnify"
                  color="gray"
                >
                </v-text-field>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
        <v-col cols="4">
          <v-row class="float-end my-xl-2" align="center">
            <v-pagination
              v-model="page"
              :length="pageCount"
              color="#F8B400"
            ></v-pagination>
            <v-switch
              color="#F8B400"
            >
            </v-switch>
            <p class="text-xl-subtitle-2 my-0">
              S platbou
            </p>
            <v-btn
              color="white"
              small
              fab
              plain
            >
              <v-icon>
                mdi-dots-vertical
              </v-icon>
            </v-btn>
          </v-row>
          <v-col cols="4">

          </v-col>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12">
          <v-data-table
            style="background-color: transparent"
            :headers="headers"
            :items="keyinfo"
            :search="search"
            hide-default-footer
            :page.sync="page"
            :items-per-page="itemsPerPage"
            @page-count="pageCount = $event"
          ></v-data-table>
        </v-col>
      </v-row>
      <speed-dial></speed-dial>
    </v-container>
  </v-app>
</template>


<script>
export default {
  name: "AdminDatabase",
  layout: "adminlayout",

  data() {
    return {
      page: 1,
      pageCount: 0,
      itemsPerPage: 6,
      cards: [
        {
          cardtitle: 'Registrovaní celkem',
          bignum: '3 675',
          styling: 'text-xl-h3 text-md-h4 text-sm-h4 ml-4',
          icon:true,
          iconRight: true,
        },
        {
          cardtitle: 'Uživatelé s min. jednou platbou',
          bignum: '368',
          styling: 'text-xl-h3 text-md-h4 text-sm-h4 ml-4',
          icon:true,
          iconRight: true,
        },
        {
          cardtitle: 'Měření (dostupná/celkem)',
          bignum: ' 26 759 / 21 674',
          styling: 'text-xl-h4 text-md-h6 my-md-1 pb-md-1 text-sm-h4 ml-4',
          icon:true,
          iconRight: true,
        },
        {
          cardtitle: 'Projekty (aktivní/celkem)',
          bignum: '426 / 2 652',
          styling: 'text-xl-h4 text-md-h6 my-md-4 pb-md-1 text-sm-h4 ml-4',
          icon:true,
          iconRight: true,
        },
        {
          cardtitle: 'Vyfakturováno',
          bignum: '1 265 000',
          styling: 'text-xl-h4 text-md-h6 my-md-4 pb-md-1 text-sm-h4 ml-4',
          icon:true,
          iconRight: true,
        },
        {
          cardtitle: 'Hardware',
          bignum: '12',
          styling: 'text-xl-h4 text-md-h6 my-md-4 pb-md-1 text-sm-h4 ml-4',
          icon:true,
          iconRight: true,
        },

      ],
      search: '',
      headers: [
        {
          text: 'Vytvořeno'.toUpperCase(),
          align: 'start',
          sortable: true,
          value: 'name',
        },
        {text: 'Role'.toUpperCase(), value: 'role'},
        {text: 'Jméno'.toUpperCase(), value: 'jmeno'},
        {text: 'Firma'.toUpperCase(), value: 'firma'},
        {text: 'Plán'.toUpperCase(), value: 'plan'},
        {text: 'Projekty'.toUpperCase(), value: 'projekt'},
        {text: 'Vyfakturováno'.toUpperCase(), value: 'paidfor'},
        {text: 'Hardware'.toUpperCase(), value: 'hardware'},
      ],
      keyinfo: [
        {
          name: '10.6.2023',
          role: 'admin',
          jmeno: 'Lorem Ipsum',
          firma: 'Lorem Ipsum',
          plan: '36(231)',
          projekt: '21(31)',
          paidfor: '26 900',
          hardware: 'ano',

        },
        {
          name: '10.6.2023',
          role: 'user',
          jmeno: 'Jaroslav Babač',
          firma: 'Mercury Technologies',
          plan: '36(231)',
          projekt: '21(31)',
          paidfor: '26 900',
          hardware: 'ano',
        },
        {
          name: '10.6.2023',
          role: 'user',
          jmeno: 'Lorem Ipsum',
          firma: 'Boar Coms',
          plan: '36(231)',
          projekt: '21(31)',
          paidfor: '26 900',
          hardware: 'ne',

        },
        {
          name: '10.6.2023',
          role: 'admin',
          jmeno: 'Jiří Chovaneček',
          firma: 'Cavernetworks',
          plan: '36(231)',
          projekt: '21(31)',
          paidfor: '26 900',
          hardware: 'ne',

        },
        {
          name: '10.6.2023',
          role: 'admin',
          jmeno: 'Josef Pavlišta',
          firma: 'Luckyworks',
          plan: '36(231)',
          projekt: '21(31)',
          paidfor: '26 900',
          hardware: 'ano',
        },
        {
          name: '10.6.2023',
          role: 'user',
          jmeno: 'Ludvík Beskyd',
          firma: 'Brisco',
          plan: '36(231)',
          projekt: '21(31)',
          paidfor: '26 900',
          hardware: 'ano',
        },
        {
          name: '10.6.2023',
          role: 'admin',
          jmeno: 'Petr Holub',
          firma: 'Voyage Navigations',
          plan: '36(231)',
          projekt: '21(31)',
          paidfor: '26 900',
          hardware: 'ano',
        },
        {
          name: '10.6.2023',
          role: 'user',
          jmeno: 'Jan Vandas',
          firma: 'Lorem Ipsum',
          plan: '36(231)',
          projekt: '21(31)',
          paidfor: '26 900',
          hardware: 'ne',

        },
        {
          name: '10.6.2023',
          role: 'user',
          jmeno: 'Jaroslav Viliš',
          firma: 'Rush Enterprises',
          plan: '36(231)',
          projekt: '21(31)',
          paidfor: '26 900',
          hardware: 'ne',

        },
        {
          name: '10.6.2023',
          role: 'user',
          jmeno: 'Martin Mazánek',
          firma: 'Forestpaw',
          plan: '36(231)',
          projekt: '21(31)',
          paidfor: '26 900',
          hardware: 'ano',
        },
      ],
    }
  },

  methods: {
    onScroll(e) {
      if (typeof window === 'undefined') return
      const top = window.pageYOffset || e.target.scrollTop || 0
      this.fab = top > 20
    },
    toTop() {
      this.$vuetify.goTo(0)
    }
  }
}
</script>

