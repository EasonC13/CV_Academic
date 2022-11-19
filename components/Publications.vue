<template lang="">
  <div id="Publications">
    <h2>Publications</h2>
    <ul>
      <li v-for="(paper, index) in papers" :key="index">
        <span
          v-html="markdownToHtml(paper.markdown)"
          class="markdown_inline"
        ></span>
        <span v-if="paper.pdf_link">
          <a :href="paper.pdf_link" target="_blank" class="link-primary">
            <i class="fa fa-file-pdf-o ml-1"></i>
          </a>
        </span>
      </li>
    </ul>
  </div>
</template>
<script>
import { marked } from "marked";
export default {
  methods: {
    markdownToHtml(markdown) {
      return marked(markdown);
    },
  },
  data() {
    return {
      papers: [
        {
          markdown:
            "Wu, C.-L., Su, Y.-D., **Chen, E.**, Chen, P.-Z., Chang, Y.-L. & Chen, H.-C. (2022). Development and Validation of Interactive Creativity Task Platform. Frontiers in Psychology, 13, Article 954946. (SSCI, IF = 4.232, 35/147 in Multidisciplinary Psychology, Q1)",
          pdf_link:
            "https://www.frontiersin.org/articles/10.3389/fpsyg.2022.954946/full",
        },
        {
          markdown:
            "**Chen, E.**, Tseng, Y.-H., You, A., Lo, K.-P., Lin, C. (2022). Preliminary Design of an AI Service to Assist Self-regulated Learning by Edge Computing. Paper present as Poster and Demo at International Conference on Artificial Intelligence in Education (AIED'22)",
          pdf_link:
            "https://link.springer.com/chapter/10.1007/978-3-031-11647-6_119",
        },
        {
          markdown:
            "**Chen, E.**, Tseng, Y.-H. (2022). A decision model for designing NLP applications. Paper presented at User Centered Natural Language Processing Workshop in Companion Proceedings of the Web Conference (WWW'22)",
          pdf_link: "https://dl.acm.org/doi/abs/10.1145/3487553.3524921",
        },
        {
          markdown:
            "**Chen, E.** (2022). The Effect of Multiple Replies for Natural Language Generation Chatbots. Paper present at Student Research Competition in Conference on Human Factors in Computing Systems Extended Abstracts (CHI EA '22)",
          pdf_link: "https://arxiv.org/pdf/2210.17209",
        },
        {
          markdown:
            "**Chen, E.**, Roche, N., Tseng, Y. H., Hernandez, W., & Shangguan, J. (2022). Conversion of Legal Agreements into Smart Legal Contracts using NLP. Technical Report at Google Summer of Code 2021",
          pdf_link: "https://arxiv.org/pdf/2210.08954.pdf",
        },
        {
          markdown:
            "Roche, N., Hernandez, W., **Chen, E.**, Siméon, J., & Selman, D. (2022). Ergo--a programming language for Smart Legal Contracts. Paper presented at the Programming Languages and the Law workshop at Principles of Programming Languages Conference (POPL'22)",
          pdf_link: "https://arxiv.org/pdf/2112.07064.pdf",
        },
        {
          markdown:
            "**Chen, E.**, Tseng, Y.-H., & Lo, K.-P. (2021). Focus Plus: Detect Learner's Distraction by Web Camera in Distance Teaching. Paper presented at the 2021 National Chair Professorship Academic Series: Teaching and Learning in Pandemic Era",
          pdf_link: "https://arxiv.org/pdf/2210.04400.pdf",
        },
        {
          markdown:
            "**Chen, E.** & Tseng, Y.-H. (2021). A chatbot platform that allow custom avatars and emotions and can provides multiple replies. Demo presented at the Taiwan Computer-Human Interaction Conference (TAICHI)",
          pdf_link: "/assets/publications/TAICHI_Demo投稿_v3.pdf",
        },
        {
          markdown:
            "**Chen, E.**, Tseng, Y.-H., Chiou, G.-L., & Yuan, C.-W. T. (2021). How the numbers of replies and avatars influence the user experience in Natural Language Generation Chatbot. Paper presented at the Taiwan Computer-Human Interaction Conference (TAICHI)",
          pdf_link: "/assets/publications/怡升_TAICHI2021_論文_final.pdf",
        },
      ],
    };
  },
};
</script>
<style>
.markdown_inline p {
  display: inline;
}
</style>
