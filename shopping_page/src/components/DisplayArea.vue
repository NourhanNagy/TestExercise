<template>
   
    <div  class="display-area">
        <div class="Productcard"  v-for="product in  productList" :key="product.id">
            <ProductCard :product="product" />
        </div>
    </div>

    
   
</template>

<script>
import ProductCard from './ProductCard.vue';
    export default{
        name: 'display-area',
        data(){
            return{
                productList: []
            }
        },
        created(){
            this.fetchList()
            
        },
        methods: {
        async fetchList() {
        try {
            const response = await fetch('https://joulia.dashboard.hamburgermenu.app/api/v1/products');
            let result = await response.json()
            this.productList = result.data.filter((product) => !!product.default_variant.image);
        } catch (error) {
          console.error('Error fetching items:', error);
        }
    },},
        components: {
    ProductCard
}
    }
</script>
<style scoped>
 .display-area {
            width: 80%;
            height: 100%;
            display: flex;
            padding-top: 50px;
            padding-inline: 10px;
            flex-wrap: wrap;
        }
 
        .Productcard{
          width: 248.41px;
          height: 383.6px;
          position: relative;
          padding-left: 5px;
          padding-right: 19px;

        }
</style>