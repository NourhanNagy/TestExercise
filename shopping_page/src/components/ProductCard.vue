<template>
            
            <!-- <div class="decoration">
              <div class="discount">
                <div>

                  40%
                </div>
              </div>
              <div class="fav">
                <div>

                  fav
                </div>
              </div>
              
            </div> -->
            <div class="product">
              <img :src="product.default_variant.image" alt="Productcard" class="product">
            </div>
            <div class="productdetails">
              <div class="productname">
                {{product.default_variant.product_title}}
              </div>
              <div class="productprice">
                
                <!-- <div class="dprice">
                  140k
                </div> -->
                <div class="ogprice">
                  {{product.default_variant.price}}
                </div>
              </div>

            </div>
            
</template>

<script>
    export default{
        name: 'productCard',
        props: {
          product : {
            type: Object
          }
        },
        created() {
          console.log("nouni testing here", this.product.default_variant)
        }
    }
</script>
<style scoped>
  
  
        .fav{
          padding-top: 10px;
          padding-right: 20px;
        }
        .fav div {
          width: 23.58px;
          height: 20.64px;
          background-color: azure;

        }
        .discount{
          padding-top: 10px;
          
        }
        .discount div {
          width: 41px;
          height: 19px;
          background-color: #fff;
          color: #c40024;
          text-align: center;
          display: flex;
          align-items: center;
          justify-content: center;
        }
        .decoration{
          width: 100%;
          display: flex;
          justify-content: space-between;
          position: absolute;
          top: 0px;
        }
        .product{
          width: 247.36px;
          height: 296.24px;
          display: flex;

        }
        .productdetails{
          width: 248.41px;
          height: 47px;
          padding-top: 10px;

        }
        .productname {
          width: 248.41px;
          height: 22px;
          text-align: start;
          text-overflow: ellipsis;
          overflow-x: hidden;
        }
         .productprice{
          width: 248.41px;
          height: 47px;
          display: flex;
          justify-content: flex-start;
          font-weight: bold;
         }
         .ogprice{
          width: 44.02px;
          height: 22px;
         }
         .dprice{
          width: 44.02px;
          height: 22px;
          text-align: start;
         }
</style>