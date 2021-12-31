<template>
    <div class="display-products-section">
        <ul class="products-container">
            <li class="product-item" v-for="productItem in state.data" :key="productItem.id">
            <ProductItems :productData="productItem"/>
             </li>
       </ul>
    </div>
    </template>
    
    <script>
    import {reactive} from 'vue'
    import ProductItems from '../components/ProductItem.vue'
    
    export default{
        components: {
            ProductItems,
        },
        setup() {
            let state = reactive({
                data: [],
            })
    
            const fetchApi = async () => {
                const response = await fetch('https://fakestoreapi.com/products/')
                const data = await response.json()
                state.data = data
                console.log(state.data)
            }
    
            fetchApi()
            
            return {
                state,
                fetchApi,
            }
                
    }
    }
            
    </script>