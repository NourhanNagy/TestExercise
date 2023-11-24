<template>
  <nav>
      <div class="logoArea">
        <h1> LOGO</h1>
        <div class="navbar">
          <div> <a href="#" id="Account">Account</a> </div>
          <div><a href="#" id="Wishlist">Wishlist</a></div>
          <div><a href="#" id="Cart">Cart</a></div>
          </div>
      </div>
      <ContentBar />
  </nav>

</template>

<script>
import ContentBar from './Content-bar.vue';

    export default{
    name: "NavigationComponent",
    components: { ContentBar }
}
</script>
<style scoped>
 
        .logoArea {
          background-color: white;
          width: 100%;
          height: 50%;
          display: flex;
          flex-direction: row;
          justify-content: space-between;
        }

        .logoArea h1 {
          padding-left: 20px;
        }
        .navbar{
    list-style-type: none;
    margin: 20px,20px;
    padding: 0;
    overflow: hidden;
    background-color: white;
  }
    div.navbar div{
        line-height: 1.2;
        margin: 20px, 20px;
        float: right;
        display: inline;
    }
    div.navbar div a {
        display: inline-block;
        line-height: 1.1;
        color: black;
        text-align: center;
        margin: 20px;
        padding: 10px;
        text-decoration: none;
    }

    div.navbar div a:hover {
      transform: scale(1);
      font-weight: bold; 
    }
</style>