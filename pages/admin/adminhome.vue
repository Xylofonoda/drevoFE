<template>
  <admin-tool-comp
    name="Přehled"
  ></admin-tool-comp>
</template>

<script>
  import AdminToolComp from "@/components/admintoolbar";
  export default {
    name:"AdminHome",
    components: {AdminToolComp},
    layout:"AllroundLayout"
  }
</script>
