<template>
  <div class="home">
    <h1> My Home</h1>
    <div class="row">
      <div class="col-md-4 " v-for="(data,index) in products" :key="index">
        <img :src="data.image" class=" rounded" @click="goToDetails(data.productId)" >

         <h3 @click="goToDetails(data.productId)" >{{data.productTitle}}</h3>
         <h1>&#8358; {{data.Price}}</h1>
       
         
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'home',
 data () {
    return {
      title: 'Home',
      products:[
      {
        productTitle:"Apple",
        image       : require('../assets/images/apple.jpg'),
        productId:1,
        Price:105 
      },
      {
        productTitle:"Cucumber",
        image       : require('../assets/images/cucumber.jpg'),
        productId:2,
        Price:155 
      },
      {
        productTitle:"Pineapple",
        image       : require('../assets/images/pineapple.jpg'),
        productId:3,
        Price:146
      },
      {
        productTitle:"Orange",
        image       : require('../assets/images/orange.jpg'),
        productId:4,
        Price:15
      },
      {
        productTitle:"Lime",
        image       : require('../assets/images/lime.jpg'),
        productId:5,
        Price:155 
      },
      {
        productTitle:"Banana",
        image       : require('../assets/images/banana.jpg'),
        productId:6,
        Price:355 
      },
       {
        productTitle:"Guava",
        image       : require('../assets/images/guava.jpg'),
        productId:7,
        Price:1505 
      },
      {
        productTitle:"Lemon",
        image       : require('../assets/images/lemo.jpg'),
        productId:8,
        Price:855 
      },
      {
        productTitle:"Cassava",
        image       : require('../assets/images/cassava.jpg'),
        productId:9,
        Price:109
      }
      ]
    }
  },
  
  methods:{
  goToDetails(prodId) {
    this.$router.push({name:'details',params:{Pid:prodId}})
  }
  }
  }
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>