<template>
  <div class="container">
    <h4 class="center">All Keeps</h4>
    <div class="row">
      <div v-for="keep in keeps" class="col s6 m4">
        <keep :keep="keep"></keep>
        <!--<div class="card hoverable" v-on:mouseenter="showAction" v-on:mouseleave="showAction">
          <div class="card-image" v-if="keep.imageUrl">
            <img :src="keep.imageUrl">
          </div>
          <div class="card-content">
            <span v-if="!keep.articleLink" class="card-title">{{ keep.title }}</span>
            <span v-if="keep.articleLink" class="card-title"><a :href="keep.articleLink">{{ keep.title }}</a></span>
          </div>
          <div class="card-action height">
            <span class="left" v-show="hoverShow"><i class="fa fa-eye"></i> {{ keep.views }} | <i class="fa fa-retweet"></i> {{ keep.timesVaulted }}</span>
            <span class="right" v-show="hoverShow"><router-link :to="'/keep/' + keep._id">add to vault</router-link></span>
          </div>
        </div>-->
      </div>
    </div>
  </div>
</template>

<script>
  import Keep from './Keep'

  export default {
    name: 'Browse',
    components: {
      Keep
    },
    data() {
      return {
        hoverShow: false
      }
    },
    computed: {
      keeps() {
        return this.$root.$data.store.state.keeps;
      }
    },
    mounted(){
      this.$root.$data.store.actions.getPublicKeeps();
    },
    methods: {
      showAction() {
        this.hoverShow = !this.hoverShow;
      }
    }
  }

</script>

<style>

</style>