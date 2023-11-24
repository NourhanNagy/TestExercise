<template>
    <div class="brand">
            <h2>Brand</h2>
              <SearchbarComponent />
              <div>
              <div v-for="brand in brandsItems" :key="brand.id">
                <label :for="brand.id">
                  <input :name="brand.id" type="checkbox">{{ brand.title }}
                </label>
              </div>
 <!---             <div>
                <label for="Lacoste (3)">
                  <input id="Lacoste (3)" type="checkbox">Lacoste (3)
                </label>
              </div>
              <div>
                <label for="Nike (13)">
                  <input id="Nike (13)" type="checkbox">Nike (13)
                </label>
              </div>
              <div>
                <label for="Levi's (3)">
                  <input id="Levi's (3)" type="checkbox">Levi's (3)
                </label>
              </div>
              <div>
                <label for="Calvin Klein (100)">
                  <input id="Calvin Klein (100)" type="checkbox">Calvin Klein (100)
                </label>
              </div>-->
             </div>
          
    </div>
</template>

<script>
    import SearchbarComponent from './Searchbar.vue';
    export default{
        name: 'BrandComponent',
        data(){
          return{
            brandsItems: []
          }
        },
        created(){
          this.fetchItems();
        },
        methods:{
          async fetchItems() {
        try {
            const response = await fetch('https://joulia.dashboard.hamburgermenu.app/api/v1/brands');
            let result = await response.json()
            this.brandsItems = result.data;
        } catch (error) {
          console.error('Error fetching items:', error);
        }
    },
        },
        components: {
          SearchbarComponent
        }
    }
</script>
<style scoped>
   .brand {
          width:100%;
          background-color: white;
          display: flex;
          flex-direction: column; 
          padding-left: 10px;
          padding-right: 5px;
        }

        .brand div, h2 {
          display: flex;
          flex-direction: column;
          align-items: start;
          margin-bottom: 0px;
          padding-bottom: 5px;
        }
          
 
</style>