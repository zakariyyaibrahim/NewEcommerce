<template>

 <div class="details">
  <h1>Details</h1>
  <h2>the product id is :{{this.$route.params.Pid}}</h2>
  <div class="col-md-12" v-for="(product,index) in products" :key="index">
     <div v-if="prodId == product.productId" align="center">
      <h1 >{{product.productTitle}}</h1>
      <img :src="product.image" class="img-fluid">
     </div>
    </div>
 </div>
</template>
<script>
 export default{
  name:'details',
  data(){
   return{
     prodId:this.$route.params.Pid,
    title:"details",
    products:[
      {
        productTitle:"Apple",
        image       : require('../assets/images/apple.jpg'),
        productId:1
      },
      {
        productTitle:"Cucumber",
        image       : require('../assets/images/cucumber.jpg'),
        productId:2
      },
      {
        productTitle:"Pineaple",
        image       : require('../assets/images/pineapple.jpg'),
        productId:3
      },
      {
        productTitle:"Orange",
        image       : require('../assets/images/orange.jpg'),
        productId:4
      },
      {
        productTitle:"Lime",
        image       : require('../assets/images/lime.jpg'),
        productId:5
      },
      {
        productTitle:"Banana",
        image       : require('../assets/images/banana.jpg'),
        productId:6
      },
       {
        productTitle:"Guava",
        image       : require('../assets/images/guava.jpg'),
        productId:7
      },
      {
        productTitle:"Lemon",
        image       : require('../assets/images/lemo.jpg'),
        productId:8
      },
      {
        productTitle:"Cassava",
        image       : require('../assets/images/cassava.jpg'),
        productId:9
      }
      ]
   }
  }
 }
</script>