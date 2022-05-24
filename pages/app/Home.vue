<template>
  <v-row>
    <v-col xl="6">
      <nuxt-link
        to="/app/userprofileview"
        style="text-decoration: none">
      <CardComponent
        label="Profil"
      ></CardComponent>
      </nuxt-link>
    </v-col>
    <v-col xl="6">
      <nuxt-link
        to="/app/plan"
        style="text-decoration: none">
      <CardComponent
        label="Plán"
      ></CardComponent>
      </nuxt-link>
    </v-col>
    <v-col xl="6">
      <nuxt-link
        to="/app/projects"
        style="text-decoration: none">
      <CardComponent
        label="Projekty"
      ></CardComponent>
      </nuxt-link>
    </v-col>
    <v-col xl="6">
      <nuxt-link
        to="/app/tutorials"
        style="text-decoration: none">
      <CardComponent
        label="Metodika"
      ></CardComponent>
      </nuxt-link>
    </v-col>
    <v-col xl="6">
      <nuxt-link
        to="/app/hardware"
        style="text-decoration: none">
      <CardComponent
        label="Hardware"
      ></CardComponent>
      </nuxt-link>
    </v-col>
    <v-col xl="6">
      <nuxt-link
        to="/app/about"
        style="text-decoration: none">
      <CardComponent
        label="About"
      ></CardComponent>
      </nuxt-link>
    </v-col>
    <v-col xl="6">
      <nuxt-link
        to=""
        style="text-decoration: none">
      <CardComponent
        label="Queue"
      ></CardComponent>
      </nuxt-link>
    </v-col>


  </v-row>
</template>

<script>
  import CardComponent from "@/components/CardComp";
  export default {
    name:"HomePage",
    components: {CardComponent},
    layout:"HomeLayout",
    data: () => ({
      model: 3,
      rounded: [
        '0',
        'sm',
        'md',
        'lg',
        'xl',
        'pill',
        'circle',
      ],
    }),

    computed: {
      radius () {
        let rounded = 'rounded'
        const value = this.rounded[this.model]

        if (value !== 'md') {
          rounded += `-${value}`
        }

        return rounded
      },
    },

  }
</script>
