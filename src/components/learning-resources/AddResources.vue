<template>
<h2>Add Resources</h2>

  <base-card>
    <form @submit.prevent = "submitData">
      <div class="form-control">
        <label for="title">Title</label>
      <input name="title" id="title" type="text" ref="titleInput"/>
      </div>
      <div class="form-control">
        <label for="description">Description</label>
        <textarea name="description" id="description" rows="3" ref="descriptionInput"/>
      </div>
      <div class="form-control">
        <label for="link">Link</label>
        <input name="link" id="link" type="url" ref="descriptionInput" />
      </div>
      <base-button type="submit"> Add Resource</base-button>
    </form>
  </base-card>
</template>

<script>
export default {
  name: "AddResources",
  components: {},
  inject: ['addResource'],
  methods: {
    submitData() {
      const enteredTitle= this.$refs.titleInput.value;
      const enteredDesc= this.$refs.descriptionInput.value;
      const enteredLink=  this.$refs.linkInput.value;


      this.addResource(enteredTitle, enteredDesc, enteredLink);
    }
  }

}
</script>

<style scoped>
label {
  font-weight: bold;
  display: block;
  margin-bottom: 0.5rem;
}

input,
textarea {
  display: block;
  width: 100%;
  font: inherit;
  padding: 0.15rem;
  border: 1px solid #ccc;
}

input:focus,
textarea:focus {
  outline: none;
  border-color: #3a0061;
  background-color: #f7ebff;
}

.form-control {
  margin: 1rem 0;
}
</style>