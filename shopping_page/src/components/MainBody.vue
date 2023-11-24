<template>
      <div class="Mainbody">
        <Sidebar />
        <DisplayArea />
      </div>
      
</template>

<script>
import DisplayArea from './DisplayArea.vue';
import Sidebar from './Sidebar.vue';
    
export default{
        name: 'MainBody',
        components: {
          Sidebar,
          DisplayArea
          
        
        }
    }
</script>
<style scoped>
    .Mainbody {
            display: flex;
            height: calc(100vh - 150px); /* Adjusted height to fill remaining space */
            width: 100%;
            display: flex;
            flex-direction: row;
            font-family: lato;
            color: #333;
            line-height: 1.6;

        }
        :root{
  --primary-color: white;
  --secondary-color: grey;
    --dark-color: #1f0128;
    --light-color:white;
    --success-color: #0d8b14;
    --fail-color: #ae2020;
}
 
</style>