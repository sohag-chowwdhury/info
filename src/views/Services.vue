<template>
  <v-container grid-list-xl>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-flex xs12 sm12 md12 lg12 xl12>
        <h2 class="pl-4">
          <span>My</span>
          <span class="blue--text">Services</span>
        </h2>
      </v-flex>
      <v-flex
        v-for="(service, i ) in services"
        :key="i"
        xs12
        sm12
        md5
        lg5
        xl5
      >
        <v-card
         class="background1"
         v-if="i == 0"
          hover
          flat
          color="transparent"
          :style="{ cursor: 'context-menu' }"
        >
          <v-card-title></v-card-title>
          <v-img
            :src="service.src"
            height="200"
            aspect-ratio="3.75"
            :alt="'Eldin do ' + service.title"
            lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif"
            contain
          ></v-img>
          <v-card-title class="justify-center">
            <v-flex text-xs-center subheading white--text font-weight-bold>{{
              service.title
            }}</v-flex>
          </v-card-title>
        </v-card>
        <v-card
         v-if="i == 1"
         class="background"
          hover
          flat
          color="transparent"
          :style="{ cursor: 'context-menu' }"
        >
          <v-card-title></v-card-title>
          <v-img
            :src="service.src"
            height="200"
            aspect-ratio="3.75"
            :alt="'Eldin do ' + service.title"
            lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif"
            contain
          ></v-img>
          <v-card-title class="justify-center">
            <v-flex  white--text  text-xs-center subheading font-weight-bold>{{
              service.title
            }}</v-flex>
          </v-card-title>
        </v-card>
      </v-flex>
      <v-flex xs12 sm12 md12 lg12 xl12>
        <h2 class="pl-4">
          <span>My</span>
          <span class="blue--text">Clients</span>
        </h2>
      </v-flex>

      <v-flex v-for="client in clients" :key="client.src" xs6 sm4 md3 lg2 xl2>
        <v-card class="background3" flat :href="client.href" target="_blank" color="transparent">
          <v-hover>
            <v-img
              slot-scope="{ hover }"
              :src="client.src"
              :alt="client.name + ' logo'"
              lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif"
              height="100"
              width="160"
              aspect-ratio="2.75"
              contain
            >
              <v-expand-transition>
                <div
                  v-if="!hover"
                  class="transition-fast-in-fast-out green v-img--reveal"
                  style="height: 100%"
                ></div>
              </v-expand-transition>
            </v-img>
          </v-hover>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {

  data () {
    return {
      clients: [
        {
          name: 'Defibids',
          src: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2Fdownload.jpg?alt=media&token=eec7b725-c185-4bfb-bf6a-71e388842e5b/',
          href: 'https://defibids.com/'
        },
        {
          name: 'NFT',
          src: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2Flogo-black.png?alt=media&token=033793c9-25b5-4d24-91cd-549ec41e0941',
          href: 'https://preview.themeforest.net/item/nftmarket-nft-marketplace-responsive-html-template/full_screen_preview/33982738?_ga=2.175093216.391442821.1653717025-1280227299.1653717025'
        },
        {
          name: 'Apukuski',
          src: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2Fapukuski-logo-png.png?alt=media&token=1d6586cc-a0b6-4821-9b1d-d935792841f9',
          href: 'https://apukuski.com/'
        },
        {
          name: 'SUS',
          src: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2Fdownload%20(1).png?alt=media&token=dec44481-b24f-4fef-bb49-fc119960378e',
          href: 'http://sus-bd.org/'
        },
        {
          name: 'Qproco',
          src: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2Fdownload.png?alt=media&token=e7e3c7d3-b9d7-425a-b0a2-e6a81347015d',
          href: 'https://qproco.com/'
        },

        {
          name: 'Yakkarrt',
          src: 'https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2Ffooter.png?alt=media&token=4180d6b2-3c12-4c72-9f43-ee2de79797e2',
          href: ''
        }

      ],
      services: [
        {
          src: 'https://img.icons8.com/color/360/000000/google-code.png',
          title: 'Web Development'
        },
        {
          src: 'https://img.icons8.com/external-kiranshastry-lineal-color-kiranshastry/360/000000/external-web-design-graph-design-kiranshastry-lineal-color-kiranshastry.png',
          title: 'Web Design'
        }
      ]
    }
  }
}
</script>
<style >
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
      #880376,
      #ee7752,
      #813d05,
      #23a6d5,
      #025844,
      #07a8e7,
      #088ac7,
      #099ad4
      
    );
    background-size: 400% 400%;
    -webkit-animation: Gradient 30s ease infinite;
    -moz-animation: Gradient 30s ease infinite;
    animation: Gradient 30s ease infinite;
  }
.background {
    color: rgb(10, 10, 10);
    background: linear-gradient(
      -45deg,
      #07e76c,
      #db1d1d,
      #2799b6,
      #225e96,
      #f504d5,
      #ee7752,
      #e73c7e,
      #23a6d5,
      #23d5ab
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
.v-img--reveal {
  opacity: 0.3;
}
</style>
