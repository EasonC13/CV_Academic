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
            "Ching-Lin Wu, Yu-Der Su, **Eason Chen**, Pei-Zhen Chen, Yu-Lin Chang and Hsueh-Chih Chen (2022). Development and Validation of Interactive Creativity Task Platform. Frontiers in Psychology, 13, Article 954946. (SSCI, IF = 4.232, 35/147 in Multidisciplinary Psychology, Q1)",
          pdf_link:
            "https://www.frontiersin.org/articles/10.3389/fpsyg.2022.954946/full",
          doi: "https://doi.org/10.3389/fpsyg.2022.954946",
        },
        {
          markdown:
            "**Eason Chen**, Yuen-Hsien Tseng, Yu-Tang You, Kuo-Ping Lo, and Chris Lin (2022). Preliminary Design of an AI Service to Assist Self-regulated Learning by Edge Computing. Paper published as poster at International Conference on Artificial Intelligence in Education 2022 (AIED)",
          pdf_link:
            "https://link.springer.com/chapter/10.1007/978-3-031-11647-6_119",
          doi: "https://doi.org/10.1007/978-3-031-11647-6_119",
        },
        {
          markdown:
            "**Eason Chen** and Yuen-Hsien Tseng (2022/04). A decision model for designing NLP applications. Paper published at User Centered Natural Language Processing Workshop in Companion Proceedings of the Web Conference 2022 (WWW)",
          pdf_link: "https://dl.acm.org/doi/abs/10.1145/3487553.3524921",
          doi: "https://doi.org/10.1145/3487553.3524921",
        },
        {
          markdown:
            "**Eason Chen** (2022/05). The Effect of Multiple Replies for Natural Language Generation Chatbots. Paper published at Extended Abstracts of the 2022 CHI Conference on Human Factors in Computing Systems (CHI EA)",
          pdf_link: "https://arxiv.org/pdf/2210.17209",
          doi: "https://doi.org/10.1145/3491101.3516800",
        },
        {
          markdown:
            "**Eason Chen**, Niall Roche, Yuen-Hsien Tseng, Walter Hernandez, and Jiangbo Shangguan (2022/03). Conversion of Legal Agreements into Smart Legal Contracts using NLP. Technical Report at Google Summer of Code 2021",
          pdf_link: "https://arxiv.org/pdf/2210.08954.pdf",
          doi: "https://doi.org/10.48550/arXiv.2210.08954",
        },
        {
          markdown:
            "Niall Roche, Walter Hernandez, **Eason Chen**, Jérôme Siméon, Dan Selman (2022/01). Ergo--a programming language for Smart Legal Contracts. Paper presented at the Programming Languages and the Law workshop at Principles of Programming Languages Conference 2022 (POPL)",
          pdf_link: "https://arxiv.org/pdf/2112.07064.pdf",
          doi: "https://doi.org/10.48550/arXiv.2112.07064",
        },
        {
          markdown:
            "**Eason Chen**, Yuen Hsien Tseng, Kuo-Ping Lo (2021). Focus Plus: Detect Learner's Distraction by Web Camera in Distance Teaching. Paper presented at the 2021 National Chair Professorship Academic Series: Teaching and Learning in Pandemic Era",
          pdf_link: "https://arxiv.org/pdf/2210.04400.pdf",
          doi: "https://doi.org/10.48550/arXiv.2210.04400",
        },
        {
          markdown:
            "**Eason Chen** , Yuen-Hsien Tseng (2021/07). A chatbot platform that allow custom avatars and emotions and can provides multiple replies. Demo presented at the Taiwan Computer-Human Interaction Conference (TAICHI)",
          pdf_link: "/assets/publications/TAICHI_Demo投稿_v3.pdf",
        },
        {
          markdown:
            "**Eason Chen** , Yuen-Hsien Tseng, Guo-Li Chiou, & Chien-Wen Tina Yuan (2021/07). How the numbers of replies and avatars influence the user experience in Natural Language Generation Chatbot. Paper presented at the Taiwan Computer-Human Interaction Conference (TAICHI)",
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
