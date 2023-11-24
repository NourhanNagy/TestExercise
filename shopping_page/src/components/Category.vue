<template>
    <div class="category">
            <h2>Category</h2>
            <SearchbarComponent />
            <div>
              <div v-for="category in categoryItems" :key="category.id">
                <label :for="category.id">
                  <input :name="category.id" type="checkbox">{{ category.title }}
                </label>
              </div>
             
              
            </div>
          </div>
              
    
</template>

<script>
    import SearchbarComponent from './Searchbar.vue';
    export default{
        name: 'CategoryComponent',
        data() {
          return {
            categoryItems: []
          }
        },
        created() {
          this.fetchItems();
        },
        methods: {
        async fetchItems() {
        try {
            const response = await fetch('https://joulia.dashboard.hamburgermenu.app/api/v1/categories');
            let result = await response.json()
            this.categoryItems = result.data;
        } catch (error) {
          console.error('Error fetching items:', error);
        }
    },},
        components:{
          SearchbarComponent
        }
    }
</script>
<style scoped>
      .category {
          width: 100%;
          background-color: white;
          display: flex;
          flex-direction: column;
          align-items: start;
          padding-left: 10px;
          padding-right: 5px;
        }

        .category div, h2 {
          display: flex;
          flex-direction: column;
          align-items: start;
          margin-bottom: 0px;
          padding-bottom: 5px;
        }
          
 
</style>