<template lang="">
  <div id="Publications">
    <h2>
      Featured Projects <br class="d-md-none" /><span class="h5"
        >(Click to know more)</span
      >
    </h2>

    <div class="row">
      <div
        class="col-md-4 align-items-stretch d-flex"
        v-for="(project, index) in projects"
        :key="index"
        @click="launchModal(index)"
      >
        <div class="card" style="width: 18rem">
          <div class="card-body">
            <h5 class="card-title">{{ project.title }}</h5>
            <p class="card-text">
              {{ project.short_desc }}
            </p>
            <img :src="project.img" class="card-img" alt="..." />
          </div>
        </div>
      </div>
    </div>

    <div>
      <!-- Button trigger modal -->
      <button
        type="button"
        class="btn btn-primary"
        data-toggle="modal"
        data-target="#exampleModalCenter"
        v-show="false"
        ref="LaunchModal"
      >
        Launch demo modal
      </button>

      <!-- Modal -->
      <div
        class="modal fade"
        id="exampleModalCenter"
        tabindex="-1"
        role="dialog"
        aria-labelledby="exampleModalCenterTitle"
        aria-hidden="true"
      >
        <div
          class="modal-dialog modal-dialog-centered modal-xl"
          role="document"
        >
          <div class="modal-content">
            <div class="modal-header">
              <h5 class="modal-title" id="exampleModalLongTitle">
                {{ projects[current_project_index].title }}
              </h5>
              <button
                type="button"
                class="close"
                data-dismiss="modal"
                aria-label="Close"
              >
                <span aria-hidden="true">&times;</span>
              </button>
            </div>
            <div class="modal-body">
              <div
                v-html="
                  markdownToHtml(projects[current_project_index].description)
                "
              ></div>
              <!-- <img
                src="/assets/publications/AIED2022_Poster.png"
                class="w-100"
              /> -->
            </div>
            <!-- <div class="modal-footer"></div> -->
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { marked } from "marked";
export default {
  methods: {
    markdownToHtml(markdown) {
      return marked(markdown);
    },
    launchModal(project_index) {
      this.current_project_index = project_index;
      this.$refs.LaunchModal.click();
    },
  },
  data() {
    return {
      current_project_index: 0,
      projects: [
        {
          title: "Focus Gift",
          short_desc:
            "Monitor users' Information Behavior to assist self regulated learning at webcam by Edge Computing",
          description: `When sitting in front of a computer screen for online learning, students can be easily distracted by other sources on the Internet. To help students im-prove their online learning experience, we implemented a highly accessible AI service, which collected facial data from the web camera to assist self-regulated learning for students with privacy protection by way of edge computing. The service can capture self-learning metrics such as eye gazing points and facial expressions. Then the captured facial streaming data can be played back by the user. All steps are done locally at the users' browser. The learners can review their online learning process to improve their learning efficiency through an interactive interface. Our preliminary evaluation showed promising feedback from real users.
### Relative Papers:
[1] [Preliminary Design of an AI Service to Assist Self-regulated Learning by Edge Computing.](https://link.springer.com/chapter/10.1007/978-3-031-11647-6_119)<br>
[2] [Focus Plus: Detect Learner's Distraction by Web Camera in Distance Teaching](https://arxiv.org/abs/2210.04400)
### Poster:
<img src='/assets/publications/AIED2022_Poster.png' width='100%'/>`,
          img: "/assets/publications/Focus_AIED22.png",
        },
        {
          title: "NLG Chatbot",
          short_desc:
            "Natural Language Generation Chatbot with Multiple Replies from various personalities to provide better dialog experience",
          description: `The AI chatbot combines NLG model (GPT3), Natural Language Understanding (NLU) Models, and Google APIs (Translation and Speech-to-Text). Now the service is experimenting with NTNU’s social science researchers on its effect of accompanying elder people in Mandarin. The key finding of my research is that users will have a better chatting experience when using an NLG chatbot that responds to users' utterances with multiple replies from various personalities. When using a chat-oriented chatbot, the key to having a good chat experience is to avoid dialog breakdown. Dialog breakdown means that users are finding it difficult to continue their conversations. The main reason causing dialog breakdown are inappropriate messages. Since AI is not perfect. We can not build an NLG chatbot that can give an ideal reply every time in an open-ended conversation. However, by providing multiple replies, we can let users be more willing to continue their conversation since they are more likely to receive at least one appropriate reply.
### Relative Papers
[1] [The Effect of Multiple Replies for Natural Language Generation Chatbots](https://arxiv.org/pdf/2210.17209.pdf)<br>
[2] [A decision model for designing NLP applications](https://dl.acm.org/doi/abs/10.1145/3487553.3524921)<br>
[3] [A chatbot platform that allow custom avatars and emotions and can provides multiple replies.](/assets/publications/TAICHI_Demo投稿_v3.pdf)<br>
[4] [How the numbers of replies and avatars influence the user experience in Natural Language Generation Chatbot.](/assets/publications/怡升_TAICHI2021_論文_final.pdf)<br>

### Poster
<img src='/assets/publications/CHI22_Poster.png' width='100%'/>`,
          img: "/assets/publications/AI_Multiple_Replies.png",
        },
        {
          title: "Smart Legal Contract",
          short_desc:
            "Conversion of Raw Text Legal Agreements into Smart Legal Contracts using NLP by Adapter-Transformers",
          description: `At Accord Project, I proposed a pipeline to automate the Smart Legal Contract creation process with several NLP models to convert rich text law contracts to the Accord Project's format. The pipeline integrated Adapter-Transformers for multi-class Named Entity Recognition to detect variables.
### Papers and Links
[1] [Conversion of Legal Agreements into Smart Legal Contracts using NLP](https://arxiv.org/abs/2210.08954)<br>
[2] [Ergo--a programming language for Smart Legal Contracts](https://arxiv.org/abs/2112.07064)<br>
[3] [GitHub: AccordProject/labs-cicero-classify](https://github.com/accordproject/labs-cicero-classify)

### Feature Photos on slide:
<h4>1. How NER Model Work?</h4>
<img src='/assets/publications/GSoC_Accord_NERDemo.png' width='100%' class='ml-3'/>
<h4>2. NER Model with Adapter-Transformers</h4>
<img src='/assets/publications/GSoC_Accord_adaptermodel.png' width='100%'  class='ml-3'/>
<img src='/assets/publications/GSoC_Accord_retrain.png' width='100%'  class='ml-3'/>
<h4>3. Using QA model to retrieve variable from raw text</h4>
<img src='/assets/publications/GSoC_Accord_QAmodel.png' width='100%' class='ml-3'/>
<h4>4. Prototype UX/UI</h4>
<img src='/assets/publications/GSoC_Accord.gif' width='100%' class='ml-3'/>`,
          img: "/assets/publications/GSoC_Accord.png",
        },
      ],
    };
  },
};
</script>
<style lang=""></style>
