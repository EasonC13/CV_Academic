<template lang="">
  <div class="" id="About">
    <div class="row mb-3">
      <div class="col">
        <h1 @click="log('Hello World')">Eason Chen</h1>
      </div>
    </div>
    <div class="row">
      <div class="col-md-4 order-md-2">
        <img
          class="img-fluid rounded mb-2 d-md-block d-none"
          src="/Eason_2022_cut_higher.jpeg"
          alt="Eason in a formal suit"
        />
        <img
          class="img-fluid rounded mb-2 d-md-none"
          src="/Eason_2022_cut.jpeg"
          alt="Eason in a formal suit"
        />
      </div>
      <div class="col-md-8 order-md-1">
        <div class="row container">
          <div class="order-md-2 text-center">
            <SocialMediaLinks />
            <a
              class="btn btn-primary btn-icon"
              href="/Eason_CV.pdf"
              target="_blank"
              rel="tooltip"
              title=""
              >CV (PDF)</a
            >
            <a
              class="btn btn-primary btn-icon ml-2"
              href="https://scholar.google.com.tw/citations?user=SMOPejMAAAAJ"
              target="_blank"
              rel="tooltip"
              title=""
              >Google Scholar</a
            >
            <!-- <a class="ml-3 btn btn-primary btn-icon" href="public/Eason_CV.pdf" target="_blank" rel="tooltip" title="">中文版網頁</a> -->
            <hr class="d-md-none" />
          </div>
          <div class="order-md-1">
            <p>
              Hi, I’m Eason from CMU HCII. In high school, I was a problem
              student, frequently skipping class and engrossed in gaming for
              over 12 hours daily. Surprisingly, gaming taught me the value of
              deliberate practice. Applying these strategies, I transformed my
              academic performance, earning numerous university awards. These
              experiences inspired me to research in Learning Sciences and
              Human-Comter Interaction, eager to discover productivity-enhancing
              educational tools. Ultimately, I aim to help others reach their
              full their potential through education. Additionally, I’m
              intrigued by the fair and transparency offered by Blockchain
              Technology and have three years of Web3 industry experience. If
              you have any cool ideas that could potentially turn into research
              papers, don't hesitate to get in touch with me
              <span class="d-md-inline d-none">
                at
                <a
                  target="_blank"
                  class="link-change-color-when-change-mode"
                  href="mailto: EasonC13@cmu.edu"
                  >EasonC13@cmu.edu</a
                ></span
              >
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      data: "HELLO",
    };
  },
  setup() {
    let a = 3;
    console.log(a);
  },
  methods: {
    log: function (data) {
      console.log(data);
    },
  },
};
</script>
<style></style>
