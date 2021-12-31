<template>
    <div class="home-page-banner-section">
        <div class="home-page-banner-text-container">
            <p class="home-page-banner-title">Has just arrivied!</p>
            <h1 class="home-page-banner-heading">Huge Summer Collection</h1>
            <p class="home-page-banner-detail">Shirts, Top Wear, Bottom Wear & much more...</p>
           
            <HomeGenderFilter />
        </div>
        <div >
            <img class="home-page-banner-image" src="https://res.cloudinary.com/ecomrce/image/upload/v1640855541/Home/01_bbpeqq.jpg" alt="banner-image" />
        </div>  
    </div>
    <div class="products-page-catogory-container">
        <DisplayProducts />
    </div>
</template>

    
<script>
import HomeGenderFilter from '../component/HomeGenderFilter.vue'

    export default{
        components: {
            HomeGenderFilter,
          

            
        },
    }   
 </script>


<style>

</style>