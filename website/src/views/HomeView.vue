<script>
import Slider from "../components/Slider.vue";
export default {
  name: "app",
  components: {
    Slider
  }
};
</script>

<template>
  <main>
    <div id="slideshow">
    <Slider />
  </div>
  <!-- <div>
      <p>Apex Enterprises offers a broad spectrum of medical and non-medical services.  Our organization is committed to providing excellent support and services to our clients.  We provide IT Solutions, Software and Cloud Services, Interface for Medical Systems, Editing/Transcription and Back-Office Services.  We undertake projects of all sizes and requirements.</p>
      <p>Our products include proprietary Pain Management and Orthopedics software, Medical Maestro.</p>
      <p>At Apex Enterprise, we work alongside our clients to provide customized turnkey solutions in patient documentation, imaging studies, medical billing etc. to enhance their productivity and to attain visible cost reduction in their various ongoing programs.  We try to create a better operating business model and the best approach for our clients thereby aiding them in improving business performance and better achieving their business goals.</p>
      <p>Apex Enterprise also provides Back Office Services with a variety of functions in multiple industries.</p>
    </div> -->
  </main>
</template>

<style scoped>
.imgs{
  width: 100%;
}
p{
  color: var(--black);
  font-size: var(--p);
  margin: 2rem;
}
</style>