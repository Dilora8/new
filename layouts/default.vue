<template>
  <div class="main">
   <div class="header">
    <Header />
    <nuxt />
   </div>
  </div>
</template>
  
  <script>
import Header from "@/components/header.vue";
export default {
  name: "DefaultLayout",
  components: {
    Header,
  },
};
</script>

<style>
</style>