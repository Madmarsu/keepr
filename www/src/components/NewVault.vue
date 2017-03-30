<template>
  <div class="container">
    <h4 class="center">Create a Vault</h4>
    <form @submit.prevent="createVault">
      <div class="input-field col s12">
        <input id="name" type="text" v-model="name" required>
        <label for="name">Name</label>
      </div>
      <div class="input-field col s12">
        <input id="image" type="text" v-model="image">
        <label for="image">Cover Image URL</label>
      </div>
      <div class="input-field col s12">
        <input id="description" type="text" v-model="description">
        <label for="description">Description</label>
      </div>
      <button type="submit" class="waves-effect waves-teal btn blue darken-4">Create</button>
    </form>
  </div>
</template>

<script>
  export default {
    name: 'new-vault',
    data() {
      return {
        name: '',
        description: '',
        image: ''
      }
    },
    mounted() {
      this.$nextTick(() => {
        console.log('initialize select..... hopefully');
        setTimeout(function () {
          $(".button-collapse").sideNav();
          $('.button-collapse').sideNav('hide');
        }, 500);
      })
      this.$root.$data.store.actions.clearSearch();
    },
    methods: {
      createVault() {
        this.$root.$data.store.actions.createVault(this.name, this.description, this.image);
      }
    }
  }

</script>

<style>

</style>