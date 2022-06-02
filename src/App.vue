<template>
  <v-app :dark="goDark">
    <v-content>
      <v-container align-center>
        <TheHeader :goDark="goDark" @changeTheme="updateTheme($event)" />

        <transition
          name="router-animation"
          mode="out-in"
          enter-active-class="animated fadeIn fast"
          leave-active-class="animated fadeOut faster"
        >
          <router-view></router-view>
        </transition>
      </v-container>

    </v-content>
     <div class="foo ">
         <p style="padding:2.1em 0em 0em 0em; margin-top: 1em; font-size:.80em !important; text-align: center; !important; color:white !important; font-weight: bold; margin:auto;;"> Contact Me Linkedin</p>
         <v-btn 
            class="background"
            fab
            dark 
            color="green"
            :href="linkdin.href"
            target="_blank"  style="margin:-9em 4em 0em 4em; width:4em; height:4em ;">
         
         
            <v-icon dark>{{ linkdin.icon }}</v-icon>
         </v-btn>
      </div>
    <svg style="margin-top: -18% !important" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
  <path fill="#0099ff" fill-opacity="1" d="M0,288L1440,224L1440,320L0,320Z"></path>
</svg>
    <TheFooter />
  </v-app>
</template>

<script>
import TheHeader from './components/TheHeader'
import TheFooter from './components/TheFooter'

export default {
  name: 'App',

  components: {
    TheHeader,
    TheFooter
  },
  data () {
    return { goDark: false,
       linkdin: {
          href: 'https://www.linkedin.com/in/chowdhury-sohag-82a6a323b/',
          icon: 'fab fa-linkedin-in'
        }
        
    } 
  },
  methods: {
    updateTheme (updatedTheme) {
      this.goDark = !updatedTheme
    }
  }
}
</script>
<style>
.background {
    color: rgb(10, 10, 10);
    background: linear-gradient(
      -45deg,
       #23a6d5,
      #025844,
      #6a02a7,
      #088ac7,
      #022a4e,
      #03885c,
       #022a4e,
      #4ab341,
      #05a1df,
      #0365b6,
      #01b646
     
    );
    background-size: 400% 400%;
    -webkit-animation: Gradient 10s ease infinite;
    -moz-animation: Gradient 10s ease infinite;
    animation: Gradient 10s ease infinite;
  }
    @-webkit-keyframes Gradient {
    0% {
      background-position: 0% 50%;
    }
    50% {
      background-position: 100% 50%;
    }
    100% {
      background-position: 0% 50%;
    }
  }

  @-moz-keyframes Gradient {
    0% {
      background-position: 0% 50%;
    }
    50% {
      background-position: 100% 50%;
    }
    100% {
      background-position: 0% 50%;
    }
  }

  @keyframes Gradient {
    0% {
      background-position: 0% 50%;
    }
    50% {
      background-position: 100% 50%;
    }
    100% {
      background-position: 0% 50%;
    }
  }
.foo {
    position:fixed;
    bottom: 2%;
    width: 12em;
    height: 4em;
    background: #024F54;
    right: 2%;
   animation-name: example;
  animation-duration: 3s;
  border-radius: 20px;
  animation-delay: 2s;

  }
  @keyframes example {
    0% {background-color:#024F54; left:87%; top:10%;}
   25% {background-color:#05666d; left:87%; top:90%;}
   50% {background-color:#053b3f; left:87%; top:92%;}
  100% {background-color:#024F54; left:87%; top:92%;}
}
@import "https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.7.0/animate.min.css";
</style>
