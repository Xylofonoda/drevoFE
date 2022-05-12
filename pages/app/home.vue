<template>
  <v-row>
    <v-col xl="6">
      <CardComponent
        label="Profil"
      ></CardComponent>
    </v-col>
    <v-col xl="6">
      <CardComponent
        label="Plán"
      ></CardComponent>
    </v-col>
    <v-col xl="6">
      <CardComponent
        label="Projekty"
      ></CardComponent>
    </v-col>
    <v-col xl="6">
      <CardComponent
        label="Metodika"
      ></CardComponent>
    </v-col>
    <v-col xl="6">
      <CardComponent
        label="Hardware"
      ></CardComponent>
    </v-col>
    <v-col xl="6">
      <CardComponent
        label="About"
      ></CardComponent>
    </v-col>
    <v-col xl="6">
      <CardComponent
        label="Queue"
      ></CardComponent>
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
