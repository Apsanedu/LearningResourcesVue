<template>
  <the-header title="Remember Remember"></the-header>
<!--  <stored-resources :resources="storedResources">-->
<!--  </stored-resources>-->
  <the-resources></the-resources>
</template>

<script>
import TheHeader from "@/components/layouts/TheHeader";
import TheResources from "@/components/learning-resources/TheResources";

export default {
  name: 'App',
  components: {
    TheHeader,
    TheResources
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

* {
  box-sizing: border-box;
}

html {
  font-family: 'Roboto', sans-serif;
}

body {
  margin: 0;
}
</style>
