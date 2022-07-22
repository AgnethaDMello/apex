<template>
<header>
    <div class="wrapper">
      
<img id="logo" src="../images/apex.png" alt="Apex Enterprises Logo"/>
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <Services title="Services" />
        <RouterLink to="/contact">Contact Us</RouterLink>
      </nav>
      
    </div>
  </header>
</template>

<script>
import Services from './ServicesView.vue'
export default {
  name: 'navbar',
  components: {
    Services
  },
}
</script>

<style scoped>
.wrapper{
  display: flex;
  padding: 1rem;
  background-color: var(--dark-brown);
  width: 100%;
}
#logo{
  justify-content: center;
  width: 10%;
  margin-right: 10%;
}
nav{
  width: 100%;
  margin-top: 0.8%;
}
</style>