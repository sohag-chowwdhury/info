<template>
  <v-layout column justify-center align-center class="mt-3 pt-0">
    <VueCompareImage
      class="hidden-md-and-down"
      hover
      :style="{ minWidth: '1300px' }"
      :sliderLineWidth="sliderLine"
      :handleSize="hSize"
      :leftImage="leftImage"
      :rightImage="rightImage"
      :sliderPositionPercentage="sliderPosition"
    />
    <VueCompareImage
      class="hidden-lg-and-up"
      hover
      :style="{ maxWidth: '400px' }"
      :sliderLineWidth="sliderLine"
      :handleSize="hSize"
      :leftImage="leftImage2"
      :rightImage="rightImage2"
      :sliderPositionPercentage="sliderPosition"
    />
    <br />

    <vue-typer
      class="headline"
      :repeat="0"
      text="Md. Sohag Chowdhury"
    ></vue-typer>
    <vue-typer
      :text="text1"
      :repeat="Infinity"
      :shuffle="false"
      initial-action="erasing"
      :pre-type-delay="70"
      :type-delay="70"
      :pre-erase-delay="1980"
      :erase-delay="150"
      erase-style="select-back"
      :erase-on-complete="false"
      caret-animation="smooth"
    ></vue-typer>
    <br />
     <br/>
    <v-flex xs12 sm8 md6 lg10 xl10>
      <v-card flat color="transparent" max-width="">
        <v-card-title primary-title>
          <div>
            <h3 class="headline mb-0 ml-1">
              <span>About</span>
              <span class="blue--text">Me</span>
            </h3>
            <div>
              <p style="font-size: 1.2em !important; opacity:0.8 ;">
                Hello!, I'm a Web App developer who is
                passionate about
                <span class="blue--text font-weight-bold"
                  >VUE , REACT, FIREBASE & Golang
                </span>
                and Co-owner of a Web Development Agency. As a sophisticated
                full-stack web app developer & I understand what it takes to
                develop your idea with dependable solutions that's take you
                closer to your goals . I have managed projects in my previous
                jobs, I have the experience of suggesting better solutions
                rather than jumping straight to projects that will have no
                impact on visitors. Whether it is a small SPA or an enterprise
                level project, me and my team aspire to get the best result for
                your endeavor with fast delivery time and competitive pricing.
              </p>
            </div>
          </div>
        </v-card-title>

        <v-card-actions class="hidden-sm-and-down">
          <v-btn
            v-for="icon in icons"
            :key="icon.icon"
            fab
            dark
            outline
            color="blue"
            :href="icon.href"
            target="_blank"
          >
            <v-icon dark>{{ icon.icon }}</v-icon>
          </v-btn>
        </v-card-actions>

        <v-card-actions class="hidden-md-and-up justify-center">
          <v-btn
            v-for="icon in icons"
            :key="icon.icon"
            small
            fab
            dark
            outline
            color="green"
            :href="icon.href"
            target="_blank"
          >
            <v-icon dark>{{ icon.icon }}</v-icon>
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import { VueTyper } from 'vue-typer'
import VueCompareImage from 'vue-compare-image'

export default {
 
  components: {
    'vue-typer': VueTyper,
    VueCompareImage
  },
  data () {
    return {
      icons: [
        { href: 'https://github.com/sohag-chowwdhury', icon: 'fab fa-github' },

        { href: 'https://twitter.com/sohag__02', icon: 'fab fa-twitter' },
        {
          href: 'https://www.linkedin.com/in/chowdhury-sohag-82a6a323b/',
          icon: 'fab fa-linkedin-in'
        },

        {
          href: 'https://www.facebook.com/chowdhury.sohag321/',
          icon: 'fab fa-facebook-f'
        },
        {
          href: 'https://www.instagram.com/sohag02.c/?hl=en',
          icon: 'fab fa-instagram'
        },
        { href: 'https://gitlab.com/sohag-chowwdhury', icon: 'fab fa-gitlab' }
      ],
      text1: ['Web App Developer', 'Web Designer', 'Front-End Developer'],
      leftImage: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2FLeft2.png?alt=media&token=ff0db6da-b35f-4d1d-af77-5582244eb57f',
      rightImage: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2Fleft1.png?alt=media&token=eccd4d43-7f54-4042-96c2-3b25b5d8ec10',
      leftImage2: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2Fleft2sm.png?alt=media&token=cd023411-5cac-48dc-9ade-5b8083ad5af5',
      rightImage2: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2Fleft1sm.png?alt=media&token=d4797d43-1411-4b26-b8e7-fa53d728b989',
      sliderLine: 0,
      hSize: 0,
      sliderPosition: 0.5
    }
  }
}
</script>
<style >
p {
  padding: 2% 0% 2% 0%;
  line-height: 2em !important;
  text-align: justify;
  font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;
  letter-spacing: 1px;

  opacity: 0.8 !important;
  
}
@keyframes rocking {
  0%,
  100% {
    transform: rotateZ(-10deg);
  }

  50% {
    transform: rotateZ(10deg);
  }
}

.vue-typer {
  font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;
  font-size: 1.5em;
  font-weight: 600;
  letter-spacing: 2px;
  margin-top:1.7em;
}
.vue-typer .custom.char.typed {
  color: rgb(7, 143, 233);
}
.vue-typer .custom.char.selected {
  color: #830640;
}

.vue-typer .custom.caret {
  animation: rocking 1s ease-in-out 0s infinite;
}
.vue-typer .custom.caret.typing {
  background-color: green;
}
.vue-typer .custom.caret.selecting {
  display: inline-block;
  background-color: #e91e63;
}
</style>
