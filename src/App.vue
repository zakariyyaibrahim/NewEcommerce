<template>
  <div id="app">
    <nav class="navbar navbar-expand-lg navbar-light bg-dark ">
  <div class="collapse navbar-collapse" id="navbarSupportedContent">
    <ul class="navbar-nav mr-auto ">
      <li class="nav-item active">
        <router-link class="nav-link text-white" to="/">Home</router-link>
     </li>
      <li class="nav-item">
         <router-link class="nav-link text-white" to="/blog">Blog</router-link>
      </li>
      <li class="nav-item active">
         <router-link class="nav-link text-white" to="/services">Our Services</router-link>
      </li>
      <li class="nav-item active">
         <router-link class="nav-link text-white" to="/contact">Contact Us</router-link>
      </li>
    </ul>
  </div>
</nav>
    
    <router-view/>
  </div>
</template>
<script>
export default {
  name: 'App'
}
</script>
<style>

</style>