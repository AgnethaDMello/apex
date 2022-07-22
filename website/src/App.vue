<!-- <script setup>
</script>

<template>
  <header>
    <div class="wrapper">
      
<img id="logo" src="/images/apex.png" alt="Apex Enterprises Logo"/>
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">Services</RouterLink>
        <RouterLink to="/contact">Contact Us</RouterLink>
      </nav>
      
    </div>
  </header>

  <RouterView/>

</template> -->

<template>
  <div id="app">
      <Navbar />
    <RouterView/>
  </div>
</template>

<script>
import Navbar from './views/Navbar.vue'
export default {
  name: 'App',
  components: {
    Navbar
  }
}
</script>

