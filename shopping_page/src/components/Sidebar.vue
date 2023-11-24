<template>
  <div class="Sidebar">
    <CategoryComponent  />
    <BrandComponent />
  </div>
</template>

<script>
    import CategoryComponent from './Category.vue';
    import BrandComponent from './Brand.vue';
    export default{
        name: 'SidebarComponent',
        components:{
          BrandComponent,
          CategoryComponent
        }
    }
</script>
<style scoped>
   .sidebar {
            background-color: red;
            width: 20%;
            height: 100%;
            display: flex;
            flex-direction: column;
            align-items: start;
        }
      
     
 
</style>