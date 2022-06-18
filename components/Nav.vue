<template lang="">
  <div>
    <nav id="navbar" class="navbar navbar-expand-lg navbar-light bg-light smart-scroll">
      <a class="navbar-brand" href="#">Eason Chen</a>
      <button id='navbarToggler' class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav mr-auto">
          <li class="nav-item active">
            <a class="nav-link" href="#About" @click.prevent="to">About</a>
          </li>
          <li class="nav-item active">
            <a class="nav-link" href="#Education" @click.prevent="to">Education</a>
          </li>
          <li class="nav-item active">
            <a class="nav-link" href="#ResearchExp" @click.prevent="to">Research</a>
          </li>
          <li class="nav-item active">
            <a class="nav-link" href="#WorkExp" @click.prevent="to">Work</a>
          </li>
          <li class="nav-item active">
            <a class="nav-link" href="#ProgrammingSkills" @click.prevent="to">Skills</a>
          </li>
          <li class="nav-item active">
            <a class="nav-link" href="#Publications" @click.prevent="to">Publications</a>
          </li>
          <li class="nav-item active">
            <a class="nav-link" href="#Speeches" @click.prevent="to">Speeches</a>
          </li>
          <li class="nav-item active">
            <a class="nav-link" href="#Honors" @click.prevent="to">Honors & Awards</a>
          </li>
          <li class="nav-item active">
            <a class="nav-link" href="#Languages" @click.prevent="to">Languages</a>
          </li>
          <li class="nav-item active">
            <a class="nav-link" href="#Recommendations" @click.prevent="to">Recommendations</a>
          </li>
          <!-- <li class="nav-item">
            <a class="nav-link" href="#">Link</a>
          </li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-expanded="false">
              Dropdown
            </a>
            <div class="dropdown-menu" aria-labelledby="navbarDropdown">
              <a class="dropdown-item" href="#">Action</a>
              <a class="dropdown-item" href="#">Another action</a>
              <div class="dropdown-divider"></div>
              <a class="dropdown-item" href="#">Something else here</a>
            </div>
          </li>
          <li class="nav-item">
            <a class="nav-link disabled">Disabled</a>
          </li> -->
        </ul>
        <!-- <form class="form-inline my-2 my-lg-0">
          <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
          <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
        </form> -->
      <ul class="navbar-nav">
        <li class="nav-item active">
          <button class="btn nav-link" v-if="!darkMode" @click="switchDark">
            <i class="fa fa-moon-o"></i> Dark Mode
          </button>
          <button class="btn nav-link" v-if="darkMode" @click="switchDark">
            <i class="fa fa-sun-o"></i> Bright Mode
          </button>
        </li>
      </ul>
      </div>
    </nav>
  </div>
</template>
<script>
export default {
  data(){
    return {
      darkMode: false
    }
  },
  async mounted(){
    // detect dark mode
    if(window.matchMedia &&
       window.matchMedia('(prefers-color-scheme: dark)').matches &&
       (await cookieStore.get("useDarkMode")).value != 'false'){
      await this.switchDark()
    }

    // add padding top to show content behind navbar
    $('body').css('padding-top', $('.navbar').outerHeight() + 'px')

    // detect scroll top or down
    if ($('.smart-scroll').length > 0) { // check if element exists
        var last_scroll_top = 0;
        let scroll_top;
        $(window).on('scroll', function() {
            scroll_top = $(this).scrollTop();
            if(scroll_top < last_scroll_top) {
                $('.smart-scroll').removeClass('scrolled-down').addClass('scrolled-up');
            }
            else {
                $('.smart-scroll').removeClass('scrolled-up').addClass('scrolled-down');
            }
            last_scroll_top = scroll_top;
        });
    }
  },
  methods: {
    hideNav(){
      let navbarToggler = $('#navbarToggler')
      if(navbarToggler[0].ariaExpanded){
        navbarToggler.click()
      }
    },
    to(event){
      this.hideNav()
      let arr = event.target.href.split("/")
      let hash = arr[arr.length - 1]
      let elmntToView = document.getElementById(hash.replace("#", ""));
      elmntToView.scrollIntoView({behavior: "instant"}); 
      window.location.hash = hash
    },
    async setUseDarkModeCookie(bool){
      const day = 24 * 60 * 60 * 1000;
      console.log('cookieStore.set')
      await cookieStore.set({
        name: "useDarkMode",
        value: bool,
        expires: Date.now() + day
      });
    },
    async switchDark(){
      let nav = document.getElementById('navbar')
      let body = document.getElementsByTagName('body')[0]
      let cards = document.getElementsByClassName('card')
      let toBeTransforms = [body, ...cards]
      if(!this.darkMode){
        this.darkMode = true
        await this.setUseDarkModeCookie(true)
        nav.classList.add('navbar-dark')
        nav.classList.add('bg-dark')
        nav.classList.remove('navbar-light')
        nav.classList.remove('bg-light')
        for (let index = 0; index < toBeTransforms.length; index++) {
          const ele = toBeTransforms[index];
          ele.style.color = 'white'
          ele.style.backgroundColor = 'black'
        }
        [...document.getElementsByClassName('text-secondary')].forEach((ele) => {
          ele.classList.add('color-light-gray')
        });
        [...document.getElementsByClassName('link-change-color-when-change-mode'),
         ...document.getElementsByClassName('btn-link')].forEach((ele) => {
          ele.classList.add('color-light-blue')
        });
      }else{
        this.darkMode = false
        await this.setUseDarkModeCookie(false)
        localStorage.removeItem('preferDarkMode')
        nav.classList.remove('navbar-dark')
        nav.classList.remove('bg-dark')
        nav.classList.add('navbar-light')
        nav.classList.add('bg-light')
        for (let index = 0; index < toBeTransforms.length; index++) {
          const ele = toBeTransforms[index];
          ele.style.color = '#212529'
          ele.style.backgroundColor = '#fff'
        }
        [...document.getElementsByClassName('text-secondary')].forEach((ele) => {
          ele.classList.remove('color-light-gray')
        });
        [...document.getElementsByClassName('link-change-color-when-change-mode'),
         ...document.getElementsByClassName('btn-link')].forEach((ele) => {
          ele.classList.remove('color-light-blue')
        });
      }
      
    }
  }
}
</script>
<style>
  .color-light-gray{
    color: #D3D3D3!important
  }
  .color-light-blue{
    color: lightblue!important;
  }
</style>
<style scoped>
  .smart-scroll{
    position: fixed;
    top: 0;
    right: 0;
    left: 0;
    z-index: 1030;
  }
  .scrolled-down{
    transform:translateY(-100%); transition: all 0.3s ease-in-out;
  }
  .scrolled-up{
    transform:translateY(0); transition: all 0.3s ease-in-out;
  }
</style>