<template>
  <v-layout row justify-center align-center wrap class="mt-4 pt-2">
    <v-flex xs12 sm12 md5 lg6 xl6 class="mt-4 pt-4">
      <h2 class="mb-4 pl-4 pt-2">Courses</h2>
      <v-card-text class="py-0">
        <v-timeline align-top dense>
          <v-timeline-item color="blue" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold blue--text">
                  Novembar 2019 -
                </div>
                <div class="caption font-weight-bold blue--text">
                  December 2020
                </div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Full Stack Web Development Course</strong>
                <div class="caption mb-2">Creative IT</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item color="blue" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold blue--text">
                  January 2019 -
                </div>
                <div class="caption font-weight-bold blue--text">
                  Novembar 2019
                </div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Build Web Apps with React & Firebase</strong>
                <div class="caption mb-2">eLearning(Udemy)</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
          <v-timeline-item color="blue" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold blue--text">
                  January 2018 -
                </div>
                <div class="caption font-weight-bold blue--text">
                  June 2018
                </div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Build Web Apps with Vue JS & Firebase</strong>
                <div class="caption mb-2">eLearning(Udemy)</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
          <v-timeline-item color="blue" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold blue--text">
                  SEP 2016 -
                </div>
                <div class="caption font-weight-bold blue--text">
                  Novembar 2016
                </div>
              </v-flex>
              <v-flex class="pl-2">
                <strong
                  >Advanced CSS and Sass: Flexbox, Grid, Animations!</strong
                >
                <div class="caption mb-2">eLearning(Udemy)</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
        </v-timeline>
      </v-card-text>
    </v-flex>
    <v-flex xs12 sm12 md4 lg6 xl6 class="mt-4 pt-2">
      <h2 class="mb-4 pl-4">Experience</h2>
      <v-card-text class="py-0">
        <v-timeline align-top dense>
          <v-timeline-item color="blue" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold blue--text">
                  DEC 2017 -
                </div>
                <div class="caption font-weight-bold blue--text">PRESENT</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Web App Developer</strong>
                <div class="caption mb-2">Freelancer</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item color="blue" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold blue--text">
                  Novembar 2021 -
                </div>
                <div class="caption font-weight-bold blue--text">May 2022</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Web Application Developer</strong>
                <div class="caption mb-2">Apukuski(Remote)</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item primary-title color="blue" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold blue--text">
                  AUG 2019 -
                </div>
                <div class="caption font-weight-bold blue--text">APR 2020</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong class="dark--text">Web Application Developer</strong>
                <div class="caption mb-2">Yakkart(Contact)</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
          <v-timeline-item color="blue" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold blue--text">
                  AUG 2017 -
                </div>
                <div class="caption font-weight-bold blue--text">APR 2018</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Web Designer</strong>
                <div class="caption mb-2">Defibids(Contact)</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
        </v-timeline>
      </v-card-text>
    </v-flex>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-flex xs12 sm12 md4 lg5 xl5 class="mx-2 pt-4">
        <h2>
          <span>Framework </span>

          <span class="blue--text">and Library</span>
        </h2>
        <br />
        <strong>VUE/NUXT</strong>
        <v-progress-linear
          v-model="buffer1"
          :buffer-value="bufferValue"
          color="blue"
          height="16"
        ></v-progress-linear>
        <strong>REACT</strong>
        <v-progress-linear
          v-model="buffer2"
          :buffer-value="bufferValue"
          color="blue"
          height="16"
        ></v-progress-linear>
        <strong>Vuetify</strong>
        <v-progress-linear
          v-model="buffer3"
          :buffer-value="bufferValue"
          color="blue"
          height="16"
        ></v-progress-linear>
        <strong>Bootstrap</strong>
        <v-progress-linear
          v-model="buffer1"
          :buffer-value="bufferValue"
          color="blue"
          height="16"
        ></v-progress-linear>
        <strong>Tailwind</strong>
        <v-progress-linear
          v-model="buffer5"
          :buffer-value="bufferValue"
          color="blue"
          height="16"
        ></v-progress-linear>
      </v-flex>
      <v-flex xs12 sm12 md4 lg5 xl5 class="mx-2 pt-4">
        <h2>
          <span>Coding</span>
          <span class="blue--text">Skills</span>
        </h2>
        <br />
        <strong>JavaScript</strong>
        <v-progress-linear
          v-model="buffer2"
          :buffer-value="bufferValue"
          color="blue"
          height="16"
        ></v-progress-linear>
        <strong>Golang</strong>
        <v-progress-linear
          v-model="buffer7"
          :buffer-value="bufferValue"
          color="blue"
          height="16"
        ></v-progress-linear>
        <strong>Node js</strong>
        <v-progress-linear
          v-model="buffer7"
          :buffer-value="bufferValue"
          color="blue"
          height="16"
        ></v-progress-linear>
        <strong>Firebase</strong>
        <v-progress-linear
          v-model="buffer2"
          :buffer-value="bufferValue"
          color="blue"
          height="16"
        ></v-progress-linear>
        <strong>HTML/CSS</strong>
        <v-progress-linear
          v-model="buffer5"
          :buffer-value="bufferValue"
          color="blue"
          height="16"
        ></v-progress-linear>
      </v-flex>
      <div class="mt-4 pt-2">
        <v-btn
          href="https://firebasestorage.googleapis.com/v0/b/student-blog-80add.appspot.com/o/personal%2FSohag_CV.pdf?alt=media&token=3e75ede5-e379-454f-9bda-1082246a6cd8"
          target="_blank"
          color="blue"
          dark
          large
        >
          Download Resume
          <v-icon right dark>fas fa-file-download</v-icon>
        </v-btn>
      </div>
    </v-layout>
  </v-layout>
</template>

<script>
export default {

  data () {
    return {
      value: 0,
      buffer1: 0,
      buffer2: 0,
      buffer3: 0,
      buffer4: 0,
      buffer5: 0,
      buffer6: 0,
      buffer7: 0,
      bufferValue: 100,
      interval: 0
    }
  },
  mounted () {
    this.startBuffer()
  },

  beforeDestroy () {
    clearInterval(this.interval)
  },

  methods: {
    startBuffer () {
      this.interval = setInterval(() => {
        this.buffer1 = 90
        this.buffer2 = 85
        this.buffer3 = 90
        this.buffer4 = 85
        this.buffer5 = 75
        this.buffer6 = 70
        this.buffer7 = 40
      }, 800)
    }
  }
}
</script>
<style >
p {
  padding: 8px;
  line-height: 1.5em !important;
  font-size: 1.05em !important;
  font-weight: 500;
  text-align: justify;
  color:black !important;
}
</style>
