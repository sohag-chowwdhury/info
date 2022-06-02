<template>
  <v-container grid-list-xl>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-flex
        v-for="(portfolio , k) in portfolios"
        :key="k"
        xs12
        sm12
        md5
        lg5
        xl5
      >
        <v-card
         v-if="k == 0"
          :to="'/portfolio/' + portfolio.title.toLowerCase()"
          hover
          flat
          color="transparent"
          height="290"
          class="background1"
        >
          <v-card-title></v-card-title>
          <v-img
            :src="portfolio.src"
            aspect-ratio="3.75"
            height="180"
            contain
          ></v-img>
          <v-card-title primary-title class="justify-center">
            <v-flex white--text text-xs-center heading font-weight-bold>{{
              portfolio.title_sub
            }}</v-flex>
          </v-card-title>
        </v-card>
         <v-card
         v-if="k == 1"
          :to="'/portfolio/' + portfolio.title.toLowerCase()"
          hover
           class="background"
          flat
          color="transparent"
          height="290"
        >
          <v-card-title></v-card-title>
          <v-img
            :src="portfolio.src"
            aspect-ratio="3.75"
            height="180"
            contain
          ></v-img>
          <v-card-title primary-title class="justify-center">
            <v-flex white--text text-xs-center heading font-weight-bold>{{
              portfolio.title_sub
            }}</v-flex>
          </v-card-title>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {

  data () {
    return {
      portfolios: [
        {
          src: 'https://img.icons8.com/external-kiranshastry-lineal-color-kiranshastry/360/000000/external-web-design-graph-design-kiranshastry-lineal-color-kiranshastry.png',
          title: 'Web',
          title_sub:'Web'
        },

        {
          src: 'https://img.icons8.com/color/360/000000/video.png',
          title: 'Video',
          title_sub:'Site demo video'
        }
      ]
    }
  }
}
</script>

<style >
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
</style>
