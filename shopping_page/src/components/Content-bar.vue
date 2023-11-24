<template>
      <div class="navigation">
        <div class="content-bar">
          <div><a href="#" id="Grocery">Grocery</a></div>
          <div><a href="#" id="Electronics">Electronics</a></div>
          <div><a href="#" id="Clothing">Clothing</a></div>
          <div><a href="#" id="Furniture">Furniture</a></div>
          <div><a href="#" id="Toys & Video Games">Toys & Video Games</a></div>
          <div><a href="#" id="Baby">Baby</a></div>
          <div><a href="#" id="Beauty">Beauty</a></div>
          <div><a href="#" id="Personal Care">Personal Care</a></div>
          <div><a href="#" id="Pets">Pets</a></div>
          <div><a href="#" id="Sports">Sports</a></div>
          <div><a href="#" id="Stationary">Stationary</a></div>
          <div><a href="#" id="Brands">Brands</a></div>
      </div>
      
      <div class="choosetype">
              <div><a href="#" id="home">Home</a></div>
              <div><a href="#" id="furniture">Furniture</a></div>
              <div><a href="#" id="Dining Tables">Dining Room Tables</a></div>
        
            </div>

      </div>

</template>

<script>
    export default{
        name: 'content-bar',
    }
</script>
<style scoped>

.navigation {
          background-color:#FBFBFB;
          width: 100%;
          height: 50%;
          display: flex;
          flex-direction: column;
        }
.content-bar{
    
    float: center;
    margin:0;
    padding: 0;
    overflow: hidden;
    background-color: whitesmoke;
    text-align: center;
   
    
    
}

div.content-bar div{
 
    display: inline-block;
    line-height: normal;
    padding: 10px;
   
  }
div.content-bar div a{
   display: inline-block;
    color: black;
    text-align: center;
    text-decoration: none;
    font-weight: bold;
    margin: 5px;
  
}

div.content-bar div a:hover{
  transform: scale(1.1); 
}
    .content-bar {
            height: 50px;
            width: 100%;
        }
        .choosetype{
  list-style-type: upper-alpha;
  float: center;
  padding: 0;
  overflow: hidden;
  text-align: left;
  line-height: 1;
  justify-self: start;
}

div.choosetype div{
  display: inline-block;
  line-height: normal;
  
}
div.choosetype div a{
  display: inline-block;
  color: black;
  text-align: center;
  text-decoration: none;
  margin: 5px;
}

div.choosetype div:not(:first-child)::before{
  content: "/";
  margin: 5px auto;
  color: black;
}
div.choosetype div a:hover{
  font-weight: bold;
}


</style>