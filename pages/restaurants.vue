<template>
    <main class="resaurant">
        <app-menu></app-menu>
        <h1>Restaurants </h1>
        <app-restaurant-info></app-restaurant-info>
        <app-footer></app-footer>
    </main>
</template>
<script>
import AppRestaurantInfo from '../components/AppRestaurantInfo.vue';
import AppFooter from '../components/AppFooter.vue';
import AppMenu from '../components/AppMenu.vue';
export default {
    components:{
        AppRestaurantInfo,
        AppFooter,
        AppMenu,
    }
}
</script>
<style lang="scss" scoped>
    
</style>