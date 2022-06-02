<template>
  <div class="background1">
    <v-footer  class="pa-3 white--text background1">
      Developed with <span class="mx-1 red--text" > Love,</span>
     
        <span class="mx-1 green--text">Vue & Vuetify</span>
      <v-spacer></v-spacer>
      <div>&copy; {{ new Date().getFullYear() }}</div>
    </v-footer>
  </div>
</template>

<script>
export default {
  
};
</script>

<style lang="stylus" scoped>

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
  -webkit-animation: Gradient 10s ease infinite;
  -moz-animation: Gradient 10s ease infinite;
  animation: Gradient 10s ease infinite;
}
.background1 {
  color: rgb(10, 10, 10);
  background: linear-gradient(
    -45deg,
    #0099FF,
    #0099FF,
    #0099FF,
     #0099FF,
    #0099FF,
    #0099FF,
     #9CC9F3,
    #0099FF,
    #0099FF
  );
  background-size: 400% 400%;
  -webkit-animation: Gradient 20s ease infinite;
  -moz-animation: Gradient 20s ease infinite;
  animation: Gradient 20s ease infinite;
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
  -webkit-animation: Gradient 5s ease infinite;
  -moz-animation: Gradient 5s ease infinite;
  animation: Gradient 5s ease infinite;
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
