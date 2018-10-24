<template>

  <v-jumbotron :gradient="gradient" dark class="elevation-5" height="none">
    <v-container fluid fill-height grid-list-xl>
      <v-layout row wrap align-center>

        <v-flex xs12 md8 text-xs-center my-4>
          <v-card id="jumbo-card" flat>
            <h1 class="display-2 mb-3">Frontend Developer</h1>
            <h2>
              Analyze, Innovate, Create
              <em style="display:block;font-size:1rem;">- React, Redux, Vue.js, Vuex, Vuetify, AngularJS, Gulp, Bootstrap, CSS, HTML, RWD, Firebase, REST API etc.</em>
            </h2>
          </v-card>
        </v-flex>

        <v-flex xs12 md4 text-xs-center my-4>
          <transition>
            <v-avatar class="grey lighten-4" v-if="isAvatarVisible" :size="avatarSize">
              <img src="../assets/photo.png">
            </v-avatar>
          </transition>
        </v-flex>

      </v-layout>
    </v-container>
  </v-jumbotron>
</template>
<script>
export default {
  name: "Header",
  data() {
    return {
      avatarSize: 250,
      gradient: "to right, #004, #1CB5E0",
      isAvatarVisible: false
    };
  },
  computed: {
    imageProfile() {
      return "../assets/photo.png";
    }
  },
  methods: {},
  mounted() {
    // To trigger animation
    this.isAvatarVisible = true;
  }
};
</script>

<style>
#jumbo-card {
  background-color: rgba(0, 0, 0, 0);
}
</style>
