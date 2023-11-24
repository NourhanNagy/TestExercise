<template>
    <footer>
      <div>
      <ul class="pagination">
          <li><a href="#" aria-label="Previous">&lt;</a></li>
          <li><a href="#">1</a></li>
          <li><a href="#">2</a></li>
          <li><a href="#">3</a></li>
          <li><a href="#" aria-label="Next">&gt;</a></li>

        </ul>
      </div>
      
     


    </footer>
</template>

<script>
      export default{
        name: 'Footer',
    }
    
</script>
<style scoped>
 .pagination {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  align-items: center;
  list-style: none;
  padding: 5px;
  background-color: white;
  color: black;
  border-color: lightgrey;
  border-style: solid;
  border-radius: 5px;
}
</style>