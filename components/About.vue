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
            <!-- <a class="ml-3 btn btn-primary btn-icon" href="public/Eason_CV.pdf" target="_blank" rel="tooltip" title="">中文版網頁</a> -->
            <hr class="d-md-none" />
          </div>
          <div class="order-md-1">
            <p>
              Eason is a senior at National Taiwan Normal University (NTNU). The
              meaning of his name 'Eason' originated from his Chinese name 怡升
              (I-Sheng), which is moving onward and upward with a joyful mind.
            </p>
            <p>
              He is a passionate researcher. As an undergraduate student, he
              participated in several research projects and wrote seven papers
              in AI, Human-Computer Interaction, Education, and Blockchain.
            </p>
            <p>
              Moreover, He loves to use programming skills and creativity to
              solve problems. Currently, he serve as Research Assistant at
              school and Blockchain R&D Engineer at Cohart.co.
            </p>
            <p>
              Eason plans to start his Ph.D. in US or UK in 2023 Fall. Now he's
              looking for program, lab, professor, and scholarship. If you have
              a potential opportunity, don't hesitate to get in touch with
              him<span class="d-md-none">.</span
              ><span class="d-md-inline d-none">
                at
                <a
                  target="_blank"
                  class="link-change-color-when-change-mode"
                  href="mailto: eason.tw.chen@gmail.com"
                  >eason.tw.chen@gmail.com</a
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
