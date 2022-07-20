<template>
  <div class="services">
    <h1>OUR SERVICES INCLUDE:</h1>
    <div class="servicelist">
      <div>
      <RouterLink class="servicelinks" to="/">- CLOUD SERVICES</RouterLink>
      </div>
      <div>
        <RouterLink class="servicelinks" to="/about">- PAIN MANAGEMENT SOFTWARE</RouterLink>
      </div>
      <div>
        <RouterLink class="servicelinks" to="/contact">- BACK OFFICE SERVICES</RouterLink>
      </div>
      <h3>- INSURANCE VERIFICATION</h3>
      <h3>- MEDICAL BILLING</h3>
      <h3>- SOFTWARE DEVELOPMENT</h3>
    </div>
  </div>
</template>

<style scoped>
.servicelist{
  font-size: var(--h3);
  font-weight: normal;
  margin-left: 5rem;
  margin-top: 2rem;
}
h1{
  margin: 1rem;
  text-shadow: 0px 8px 8px rgba(0, 0, 0, 0.25);
}
.servicelinks{
  color: var(--moss-green);
}
@media (hover: hover) {
  a:hover {
    background-color: var(--grey);
  }
}
</style>
