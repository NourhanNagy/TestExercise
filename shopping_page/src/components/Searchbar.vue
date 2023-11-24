<template>
    <div class="searchbar">
                <input type="text" placeholder="Search by category" class="searchInput" />
     </div> 
</template>

<script>
    export default{
        name: 'SearchbarComponent',
    }
</script>
<style scoped>
    .searchbar {
          padding: 0px;
          border-radius: 5px; /* Adjust the border-radius to make it more or less rounded */
          outline: none; /* Remove the default focus outline */
          background-color:#FBFBFB;
          display: flex;
          flex-direction: row;
        }
          
    .searchInput {
        background-color: #f3f3f3;
        border-style: none;
        width: 262px;
        height: 32px;
        /* padding-left: 10px; */

        border-radius: 50px;
    }
    .searchInput::placeholder {
        padding-left: 10px;
    }
 
</style>