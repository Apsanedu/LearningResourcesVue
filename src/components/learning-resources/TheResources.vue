<template>
<base-card>
  <base-button @click="setSelectedTab('stored-resources')">Stored Resources</base-button>
  <base-button @click="setSelectedTab('add-resources')">Add Resources</base-button>
</base-card>
  <component :is="selectedTab"></component>
</template>

<script>
import StoredResources from "@/components/learning-resources/StoredResources";
import AddResources from "@/components/learning-resources/AddResources";

export default {
  components: [ 'StoredResources', 'AddResources'],
  name: "TheResources",
  data(){
    return {
      selectedTab: 'stored-resources',
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
        }]
    }
  },
  methods: {
    setSelectedTab (tab){
      this.selectedTab = tab;
    }
  },
provide(){
  return{
    resources: this.storedResources
  };
},
}

</script>

<style scoped>

</style>