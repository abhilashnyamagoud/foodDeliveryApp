<template>
  <div>
  <div class="content">
    <app-menu></app-menu>
    <app-header></app-header>
    <app-resaurant-info :datasource="fooddata" ></app-resaurant-info>
    <app-footer></app-footer>
  </div>
  </div>
</template>

<script>
import AppMenu from '../components/AppMenu.vue';
import AppHeader from '../components/AppHeader.vue';
import AppResaurantInfo from '../components/AppRestaurantInfo.vue'
import AppFooter from '../components/AppFooter.vue';
import {mapState} from 'vuex';

export default {
  components:{
    AppMenu,
    AppHeader,
    AppResaurantInfo,
    AppFooter,
  },
  computed:{
    ...mapState(["fooddata"])
  },
};
</script>

<style>

</style>
