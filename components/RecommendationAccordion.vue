<template lang="">
  <div class="" id="Recommendations">
    <h2>Recommendations</h2>
    <div class="accordion" id="accordionTestimonial">
      <div class="card" v-for="(recommendation, index) in recommendations" :key="index">
        <div class="" :id="`accordionTestimonialHeading_${index}`">
          <h5 class="ml-3 mb-0">
            <div class="" type="button" data-toggle="collapse" :data-target="`#accordionTestimonialCollapse_${index}`" aria-expanded="true" :aria-controls="`accordionTestimonialCollapse_${index}`">
              <div class="d-flex flex-row align-items-center transform-darkmode">
                <img :src="recommendation.image" width="50" class="rounded-circle">
                <div class="d-flex flex-column ml-2">
                  <span>{{recommendation.name}}</span>
                  <span class="h6 mb-0 font-weight-normal">{{recommendation.title}}</span>
                  <span class="h6 font-weight-normal text-secondary">{{recommendation.date}}, {{recommendation.relation}}</span>
                </div>
              </div>
            </div>
          </h5>
        </div>
        <div :id="`accordionTestimonialCollapse_${index}`" class="collapse" :aria-labelledby="`accordionTestimonialHeading_${index}`" data-parent="#accordionTestimonial">
          <div class="card-body pt-0 pb-2">
            <p class="mb-1"
            v-for="(text, index) in recommendation.text.split('\n')" :key="index">
              {{text}}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  mounted() {
    document.getElementById('accordionTestimonialCollapse_0').classList.add("show")
  },
  data(){
    return {
      recommendations: [
        {
          name: 'Yuen-Hsien Tseng',
          title: 'Distinguished Professor at National Taiwan Normal University',
          relation: 'Yuen-Hsien was Eason’s thesis advisor at NTNU',
          date: 'May 22, 2022',
          image: '/assets/recommendation_imgs/samTseng.png',
          text_full: `Among the undergraduate students I have taught for more than 20 years, Eason is the most clever and diligent student I have ever seen so far. Moreover, he is enthusiastic about learning techniques and applications of Education, AI, NLP, and Blockchain. Therefore, he has developed quite a few applications that impressed me, examples including an embedding-based move recommender via LINE chatbot (with similar movies in 2-D visualized graph in the LINE chatbot interface), not only duplicating our research output (an emotional chatbot system) but also improving the system by allowing multiple responses with a solid evaluation experiment, and an edge-computing based eye-tracking and emotional face recognition system applied in an online learning scenario to improve individual's self-regulated learning.\n\n He did not only develop application systems quickly but also evaluated their use in practical applications based on what he learned in his major, i.e., Learning Science, which often integrates the knowledge from psychology, .human behavior, advanced statistics, and information technology.\n\n He also devoted himself to scientific paper writing and therefore has several papers accepted in refereed international conferences. I have never heard of any undergraduate students in Taiwan who could have more than 7 papers accepted before their graduation, except Eason.\n\n I would like to keep him beside me to do more research and develop more exciting applications in NLP, AI, or education. However, I also wish him to go outside to experience a broader career opportunity which I believe will benefit us all, as he is able to do something useful in academics and industrial sectors.\n\n`,
          text: `Eason is the most clever and diligent student I have ever seen so far. He is enthusiastic about learning techniques and applications, such as Education, AI, NLP, and Blockchain, and has developed quite a few applications that impressed me. \nMoreover, He did not only develop application systems quickly but also evaluated their use in practical applications based on what he learned in his major, i.e., Learning Science. \nLastly, He also devoted himself to scientific paper writing and therefore has several papers accepted in refereed international conferences. I have never heard of any undergraduate students in Taiwan who could have more than 7 papers accepted before their graduation, except Eason.`,
        },
        {
          name: 'George Chu',
          title: 'Founder and CEO of FiO',
          relation: 'George Managed Eason directly at FiO',
          date: 'May 20, 2022',
          image: '/assets/recommendation_imgs/GeorgeChu.png',
          text_full: null,
          text: `Eason is a very talented, energetic, and self-disciplined person who gives 100% focus on things he is interested. During his work with me, he has demonstrated a great level of creativity with a great mentality for entrepreneurship. He is also a fast learner and loves discovering new technologies with strong desire for new and more knowledge. He possesses a huge potential to be explored and guided with a creative mind. He does have few areas to be further improved but I believe with right mind set, he will easily grow to the next level with no doubt.`,
        },
        {
          name: 'Niall Roche',
          title: 'Head of Distributed Systems Engineering at Mishcon de Reya LLP & Senior Teaching Fellow at UCL School of Management',
          relation: `Niall was Eason's mentor at Google Summer of Code`,
          date: 'September 24, 2021',
          image: '/assets/recommendation_imgs/NiallRoche.png',
          text_full: null,
          text: `Eason's passion for his Google Summer of Code project was matched by his technical capabilities, and his continued hunger to learn and improve. He has been a wonderful mentee and continues to be a passionate contributor to OSS projects. He has a range of technical abilities from Web Development, Machine Learning (in particular, NLP) and also in Blockchain and Distributed Ledger Technologies. He would be a great asset to any team.`,
        }
      ]
    }
  }
}
</script>
<style lang="">
  
</style>