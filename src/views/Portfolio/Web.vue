<template>
  <v-container grid-list-xl>
    <h2 class="pl-4">
      <span>Web</span>
      <span class="green--text">Portfolio</span>
    </h2>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-dialog
        v-model="project.dialog"
        lazy
        max-width="1000"
        v-for="(project , j) in projects"
        :key="j"
      >
        <template v-slot:activator="{ on }">
          <v-flex xs12 sm6 md4 lg4 xl4 v-on="on" >
            <v-card :class="j % 2 == 0 ? 'background1':'background'" hover flat color="transparent">
              <v-img
                :src="project.poster"
                :alt="project.title"
                height="230"
                lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif"
              ></v-img>
              <v-card-title style="font-weight:600;"   primary-title class="justify-center white--text">{{project.title}}</v-card-title>
            </v-card>
          </v-flex>
        </template>
        <v-card v-if="project.dialog">
          <v-img :src="project.poster"></v-img>
          <v-card-text>
            <h3 class="headline mb-0">
              <span>Technology</span>
            </h3>
            <v-chip color="green" text-color="white">{{project.tech.tech1}}</v-chip>
            <v-chip color="green" text-color="white">{{project.tech.tech2}}</v-chip>
            <v-chip color="green" text-color="white">{{project.tech.tech3}}</v-chip>
            <v-chip color="green" text-color="white">{{project.tech.tech4}}</v-chip>
          </v-card-text>
          <v-card-actions>
            <v-btn flat large dark color="green" :href="project.git" target="_blank">
              <v-icon left>fab fa-github</v-icon>GitHub
            </v-btn>

          </v-card-actions>
        </v-card>
      </v-dialog>
    </v-layout>
  </v-container>
</template>

<script>
export default {

  data () {
    return {
      dialog: false,
      projects: [
        {
          dialog: false,
          title: 'Resappy',
          git: 'https://github.com/sohag-chowwdhury/Resappy',
          tech: {
            tech1: 'Vue js',
            tech2: 'JavaScript',
            tech3: 'Vuetify',
            tech4: 'HTML/CSS'
          },
          poster: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2FprojectImage%2FResappy.png?alt=media&token=ad4d2e54-7f84-40ca-a8d9-c32ab074e72b'
        }, 
        {
          dialog: false,
          title: 'This Site',
          git: '',
          demo: 'https://eldin.space/',
          tech: {
            tech1: 'VUE',
            tech2: 'Vuetify',
            tech3: 'Javascript',
            tech4: 'HTML/CSS'
          },
          poster: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2FProfile.png?alt=media&token=37da6fcb-c1e2-4dc2-818c-7aef7789b1e5'
        },
         {
          dialog: false,
          title: 'Apukuski Front-End & Back-End',
          git: 'https://github.com/sohag-chowwdhury/Apukuski',
          demo: 'https://eldin.space/',
          tech: {
            tech1: 'VUE',
            tech2: 'Golang',
            tech3: 'PostgreSQL',
            tech4: 'Google Map API'
          },
          poster: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2FprojectImage%2FApukuski.png?alt=media&token=87543a89-5144-4bb8-a45c-78af05fe0b1b'
        },
        {
          dialog: false,
          title: 'ALTA EVENT',
          git: 'https://github.com/sohag-chowwdhury/REACT_ALTA',
          tech: {
            tech1: 'React',
            tech2: 'Firebase',
            tech3: 'Google Map',
            tech4: 'HTML/CSS'
          },
          poster: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2FprojectImage%2FAltra.png?alt=media&token=f5d3643f-793c-4527-925f-a0b0ca280bbe'
        },
        {
          dialog: false,
          title: 'NFT PWA',
          git: 'https://github.com/sohag-chowwdhury/NFT',
          tech: {
            tech1: 'VUE',
            tech2: 'Firebase Social auth',
            tech3: 'Vuexfire',
            tech4: 'PWA'
          },
          poster: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2FprojectImage%2FNFT.png?alt=media&token=f01cc0f1-4bce-417a-8b9b-6a0fb2a88931'
        },
        {
          dialog: false,
          title: 'Yakkart Marketplace',
          git: 'https://github.com/sohag-chowwdhury/Yakkart-dev',
          tech: {
            tech1: 'VUE',
            tech2: 'Firebase',
            tech3: 'Leaflet',
            tech4: 'Bootstrap'
          },
          poster: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2FprojectImage%2FYakkart%20Marketplace.png?alt=media&token=f2353ac7-d630-4b61-bb7b-01a59f8241ae'
        },
        {
          dialog: false,
          title: 'Social Upliftment Society (SUS)',
          git: 'https://github.com/sohag-chowwdhury/SUS',
          tech: {
            tech1: 'VUE',
            tech2: 'JavaScript',
            tech3: 'Vuetify',
            tech4: 'HTML/CSS'
          },
          poster: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2FprojectImage%2FSUS.png?alt=media&token=fbe283ce-3797-451b-a872-d239b5be0053'
        },
        {
          dialog: false,
          title: 'Send PDF to physical mail',
          git: 'https://github.com/sohag-chowwdhury/sendPdf',
          tech: {
            tech1: 'VUE',
            tech2: 'Golang',
            tech3: 'Stripe',
            tech4: 'LOB API'
          },
          poster: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2FprojectImage%2FLob.png?alt=media&token=36684a7d-3590-4bd4-a2ce-1c9bd02d1768'
        },
        {
          dialog: false,
          title: 'Defibids',
          git: 'https://github.com/sohag-chowwdhury/Defibids',
          tech: {
            tech1: 'Vue',
            tech2: 'Javascript',
            tech3: 'Vuetify',
            tech4: 'HTML/CSS'
          },
          poster: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2FprojectImage%2FDefibeds.png?alt=media&token=f1c12e88-2539-40ac-a525-083f3cb2f1ca'
        },
        {
          dialog: false,
          title: 'Beet Front-End',
          git: 'https://github.com/sohag-chowwdhury/BeetInfo',
          tech: {
            tech1: 'Vue',
            tech2: 'Bootstrap',
            tech3: 'JavaScript',
            tech4: 'HTML/CSS'
          },
          poster: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2FprojectImage%2Fbeet.png?alt=media&token=c7bb742b-ed60-4864-9a78-02ccaf7cb9ee'
        },
        {
          dialog: false,
          title: 'Mizuex',
          git: 'https://github.com/sohag-chowwdhury/Mizux',
          tech: {
            tech1: 'HTML/CSS',
            tech2: 'Bootstrap',
            tech3: 'JavaScript',
            tech4: 'jQuery'
          },
          poster: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2FprojectImage%2FMIzuex.png?alt=media&token=d97af07a-7cbb-4237-a4e3-03e42bf9d8ea'
        },
        {
          dialog: false,
          title: 'Buying House',
          git: 'https://github.com/sohag-chowwdhury/buying_house',
          tech: {
            tech1: 'Vue',
            tech2: 'Bootstrap',
            tech3: 'JavaScript',
            tech4: 'Firebase'
          },
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
      #09021b,
      #250321,
      #300d03,
      #291302,
      #f77801,
      #080c0b,
      #f57904,
      #000102,
      #020808

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
     #3e04d1,
      #250321,
      #03bb3a,
      #291302,
      #016cf7,
      #080c0b,
      #026b72,
      #000102,
      #020808

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
       #04475f,
      #033025,
      #6a02a7,
      #088ac7,
      #022a4e,
      #03885c,
       #022a4e,
      #4ab341,
      #01161f,
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
