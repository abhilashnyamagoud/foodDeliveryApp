<template>
    <main class="resaurant">
        <app-menu></app-menu>
        <div class="restaurantheading p-4 bg-info">
            <h1 class="text-light display-4">Restaurants </h1>
            <app-select @change="selectedRestaurant =$event" ></app-select>
            <!-- <pre>{{$data}} </pre> -->
        </div>
        <app-restaurant-info :datasource="filteredRestaurants"></app-restaurant-info>
        <app-footer ></app-footer>
    </main>
</template>
<script>
import AppRestaurantInfo from '../components/AppRestaurantInfo.vue';
import AppFooter from '../components/AppFooter.vue';
import AppMenu from '../components/AppMenu.vue';
import AppSelect from '../components/AppSelect.vue';

import {mapState} from 'vuex'

export default {
    components:{
        AppRestaurantInfo,
        AppFooter,
        AppMenu,
        AppSelect,
    },
    data(){
        return{
            selectedRestaurant:"",
        };
    },
    computed:{
        ...mapState(['fooddata']),
        filteredRestaurants(){
            if(this.selectedRestaurant){
                return this.fooddata.filter(el=>{
                    return el.name.toLowerCase().includes(this.selectedRestaurant)
                });
            }
            return this.fooddata;
        }
    }
}
</script>
<style lang="scss" scoped>
    
</style>