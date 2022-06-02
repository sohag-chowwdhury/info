<template>
  <v-container grid-list-xl>
    <h2 class="pl-4">
      <span>Video</span>
      <span class="green--text">Portfolio</span>
    </h2>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-dialog
        v-model="video.dialog"
        lazy
        max-width="800"

        v-for="(video,m) in videos"
        :key="m"
      >
        <template v-slot:activator="{ on }">
          <v-flex xs12 sm6 md4 lg4 xl4 v-on="on">
            <v-card :class="m % 2 == 0 ? 'background1':'background'"  min-height="270" max-height="270" hover flat color="transparent">
              <v-img
                :src="video.poster"
                aspect-ratio="1.7778"
                :alt="video.title"
                lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif"
                contain
              ></v-img>
              <v-card-title style="font-weight:600;"  primary-title class="white--text justify-center">{{
                video.title
              }}</v-card-title>
            </v-card>
          </v-flex>
        </template>
        <v-card v-if="video.dialog">
          <plyr>
            <div class="plyr__video-embed">
              <iframe
                :src="video.href"
                allowfullscreen
                allowtransparency
                allow="autoplay"
              ></iframe>
            </div>
          </plyr>
        </v-card>
      </v-dialog>
    </v-layout>
  </v-container>
</template>

<script>
import { PlyrVideo } from 'vue-plyr'

export default {

  components: { plyr: PlyrVideo },
  data () {
    return {
      dialog: false,
      videos: [
        {
          dialog: false,
          title: 'Defibids | Vue | Bootstrap | Front-End',
          href: 'https://www.youtube.com/embed/Wa4_z28WMa0',
          type: 'text/html',
          youtube: 'Wa4_z28WMa0',
          poster: 'https://img.youtube.com/vi/Wa4_z28WMa0/maxresdefault.jpg'
        },
        {
          dialog: false,
          title: 'Resappy | Vue JS | Vue | Vuetify | Javascript',
          href: 'https://www.youtube.com/embed/8VG4SZoNBzU',
          type: 'text/html',
          youtube: '8VG4SZoNBzU',
          poster: 'https://img.youtube.com/vi/8VG4SZoNBzU/maxresdefault.jpg'
        },
        {
          dialog: false,
          title: 'Apukuski | Golang | Vue | Multiple Location | Google Map',
          href: 'https://www.youtube.com/embed/TouABCikSVw',
          type: 'text/html',
          youtube: 'TouABCikSVw',
          poster: 'https://img.youtube.com/vi/TouABCikSVw/maxresdefault.jpg'
        },
        {
          dialog: false,
          title: 'This Site',
          href: 'https://www.youtube.com/embed/twwxyEiYxrA',
          type: 'text/html',
          youtube: 'twwxyEiYxrA',
          poster: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2FProfile.png?alt=media&token=37da6fcb-c1e2-4dc2-818c-7aef7789b1e5'
        },
        {
          dialog: false,
          title: 'Beet | Vue | Bootstrap | Javascript | Front-End',
          href: 'https://www.youtube.com/embed/fsL1B8Xis5s',
          type: 'text/html',
          youtube: 'fsL1B8Xis5s',
          poster: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2FCrypto.PNG?alt=media&token=fe7e66ab-50ad-4892-bf8b-ae64d43638f9'
        },
        {
          dialog: false,
          title: 'ALT | React | Firebase | Google Map',
          href: 'https://www.youtube.com/embed/Nlfd2HpAcVw',
          type: 'text/html',
          youtube: 'Nlfd2HpAcVw',
          poster: 'https://img.youtube.com/vi/Nlfd2HpAcVw/maxresdefault.jpg'
        },
        {
          dialog: false,
          title: 'NFT | Vue | Vuexfire | Firebase Auth | PWA | SPA Web App',
          href: 'https://www.youtube.com/embed/FUOo6x1y6QY',
          type: 'text/html',
          youtube: 'FUOo6x1y6QY',
          poster: 'https://img.youtube.com/vi/FUOo6x1y6QY/maxresdefault.jpg'
        },
        {
          dialog: false,
          title: 'Send PDF to physical Mail | LOB API | Vue JS | Stripe | Firebase | Vuetify',
          href: 'https://www.youtube.com/embed/7cS1rJn3vHc',
          type: 'text/html',
          youtube: '7cS1rJn3vHc',
          poster: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2FaaaaLob.PNG?alt=media&token=7c101f25-c57b-42b3-b41f-89a762c5e45b'
        },
        {
          dialog: false,
          title: 'SUS | Vue js | Animated CSS | Vuetify',
          href: 'https://www.youtube.com/embed/990fEr15FkY',
          type: 'text/html',
          youtube: '990fEr15FkY',
          poster: 'https://img.youtube.com/vi/990fEr15FkY/maxresdefault.jpg'
        },
        {
          dialog: false,
          title: 'Yakkart | Vue | Firebase | Leaflet js | Bootstrap | Realtime Database',
          href: 'https://www.youtube.com/embed/QrZor5PwSDY',
          type: 'text/html',
          youtube: 'QrZor5PwSDY',
          poster: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2F1AAAYAkkart.PNG?alt=media&token=ac63374d-e8bb-4472-8d8a-7f01995d8122'
        },
        {
          dialog: false,
          title: 'Mizuxe | Bootstrap | HTML | CSS',
          href: 'https://www.youtube.com/embed/MbkZYTcLmXI',
          type: 'text/html',
          youtube: 'MbkZYTcLmXI',
          poster: 'https://img.youtube.com/vi/MbkZYTcLmXI/maxresdefault.jpg'
        },
        {
          dialog: false,
          title: 'Buying house | Vue | Firebase | Vuetify',
          href: 'https://www.youtube.com/embed/kc0guP7-cwg',
          type: 'text/html',
          youtube: 'kc0guP7-cwg',
          poster: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2F111BBBBuyeing.PNG?alt=media&token=8cb1bf06-61d2-4fb8-9433-965cb56ad8e7'
        }

      ]
    }
  }
}
</script>

<style  scoped>
@import "../../../node_modules/vue-plyr/dist/vue-plyr.css";
.background3 {
    color: rgb(10, 10, 10);
    background: linear-gradient(
      -45deg,
      #020f1b,
      #250321,
      #300d03,
      #291302,
      #021d27,
      #042e24,
      #033a50,
      #02364e,
      #032f41

    );
    background-size: 400% 400%;
    -webkit-animation: Gradient 30s ease infinite;
    -moz-animation: Gradient 30s ease infinite;
    animation: Gradient 30s ease infinite;
  }
.background1 {
    color: rgb(10, 10, 10);
    background: linear-gradient(
      -45deg,
      #022a4e,
      #0e8803,
      #05a1df,
      #0365b6,
      #23a6d5,
      #025844,
      #6a02a7,
      #088ac7,
      #57e903

    );
    background-size: 400% 400%;
    -webkit-animation: Gradient 10s ease infinite;
    -moz-animation: Gradient 10s ease infinite;
    animation: Gradient 10s ease infinite;
  }
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
</style>
