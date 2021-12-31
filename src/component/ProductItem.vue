<template>
    <div class="row">
      <q-card >
        <q-card-section>
            <img class="product-image" :src="productData.image" alt="product" />
          <div class="product-title">{{productData.title}}</div>
          <div class="width-100">
            <q-rating size="18px" v-model="productData.rating.rate" color="primary" />
            <span class="text-caption text-grey q-ml-sm">{{productData.rating.rate}}</span><span class="text-caption text-grey q-ml-sm">({{productData.rating.count}})</span>
          </div>
        </q-card-section>
      </q-card>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue'
  
  
  export default {
      props: ['productData'],
    setup (props) {
        console.log(props.productData.image)
      // return {
      //   stars: ref(4)
      // }
    }
  }
  </script>
  