<template>
  <div>
    <Nav></Nav>
    <div class="container">
      <div class="mt-5 d-md-block d-none"></div>
      <div class="mt-3 d-md-none"></div>
      <About />
      <hr />
      <Education />
      <hr />
      <ResearchExp />
      <hr />
      <WorkExp />
      <hr />
      <ProgrammingSkills />
      <hr />
      <FeatureProjects />
      <hr />
      <Publications />
      <hr />
      <Speeches />
      <!-- <hr>
      <PublicSpeakingExp/> -->
      <hr />
      <HonorAwards />
      <hr />
      <Languages />
      <hr />
      <!-- <Testimonial/>
      <TestimonialColumnVer/> -->
      <RecommendationAccordion />
    </div>
    <Footer />
  </div>
</template>
<script>
export default {
  setup() {
    // Replace the current URL with a new one
    window.location.replace("https://eason.phd");
  },
};
</script>
<style></style>
