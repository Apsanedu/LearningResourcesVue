<template>
<base-card>
  <base-button @click="setSelectedTab('stored-resources')">Stored Resources</base-button>
  <base-button @click="setSelectedTab('add-resources')">Add Resources</base-button>
</base-card>
</template>

<script>
import StoredResources from "@/components/learning-resources/StoredResources";
import AddResources from "@/components/learning-resources/AddResources";

export default {
  components: [ 'StoredResources', 'AddResources'],
  name: "TheResources",
  data() {
    return {
      selectedTab: 'stored-resources'
    }
  },
  methods: {
    setSelectedTab (tab) {
      this.selectedTab = tab;
    }
  }
}

</script>

<style scoped>

</style>