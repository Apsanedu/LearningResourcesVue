<template>
  <the-header title="Remember Remember"></the-header>
  <stored-resources :resources="storedResources">
  </stored-resources>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import StoredResources from "@/components/learning-resources/StoredResources";
import TheHeader from "@/components/layouts/TheHeader";

export default {
  data() {
    return {
      storedResources: [{
        id: 'official-guide',
        title: 'The Official Guide',
        description: 'This is important guide cause it\'s official.',
        link: 'https://vuejs.org'
      },
        {
        id: 'google-guide',
        title: 'Google.com link',
        description: 'Search with Google',
        link: 'https://google.com'
        }
    ]}
  },
  name: 'App',
  components: {
    // HelloWorld
    StoredResources,
    TheHeader,
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
