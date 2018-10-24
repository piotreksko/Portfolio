<template>
    <v-container class="projects" grid-list-xl>
        <h1 class="display-3">My projects</h1>
        <v-layout wrap>
            <v-flex xs12 sm6 lg4 v-for="project in projects" :key="project.id">
                <v-card class="mediaImage" hover height="100%">
                    <v-img height="420px" :src="project.image">
                    </v-img>
                    <v-divider />
                    <v-card-actions align-center>
                        <v-btn :href="project.git" target="_blank" color="accent2">Code</v-btn>
                        <v-btn :href="project.live" target="_blank" color="accent">Live</v-btn>
                    </v-card-actions>
                    <v-card-text>
                        <h2 v-html="project.name" class="mb-2"></h2>
                        <h3 justify-center v-html="project.desc" class="mb-2"></h3>
                        <v-chip class="white--text" color=info small v-for="tag in project.tags" :key="tag.id">
                            {{ tag }}
                        </v-chip>
                    </v-card-text>
                </v-card>
            </v-flex>
        </v-layout>
    </v-container>
</template>
<script>
export default {
  name: "Projects",
  data() {
    return {
      projects: [
        {
          name: "Macao - cards game",
          desc:
            "I am currently working in a React/Redux implementation of this game. You can play a 1v1 game of Macao against AI. It is written in JavaScript (ES6) with the use of jQuery library. I created it to practice and improve my JavaScript skills. I started this project back in the day when I did not know any framework such as Vue, React or Angular, thus it's been developed using jQuery.",
          git: "https://github.com/piotreksko/Makao",
          live: "https://makao-win-counter.firebaseapp.com/",
          image: require("../assets/makao.jpg"),
          tags: ["ES6", "jQuery", "Firebase", "React/Redux in progress"]
        },
        {
          name: "Orienteering event (with chat)",
          desc:
            "This is an imaginary Orienteering Event website that I have created as a side project. The goal is to create a website that will include all information about the event and handle new event entries. Some additional features will be included such as chat or interactive map that will let the user add a mark on the map and inform other competitors that he has free space in his car and is willing to take other competitors to the event from his area.",
          git: "https://github.com/piotreksko/Orienteering-event",
          live: "https://orienteering-event.firebaseapp.com/",
          image: require("../assets/orienteering.jpg"),
          tags: ["Vue.js", "Vuex", "Vuetify", "Firebase"]
        },
        {
          name: "Ghost producer for hire",
          desc:
            "My own website promoting my music production services. Includes sample audio playback",
          git: "https://github.com/piotreksko/Ghost-producer-for-hire",
          live: "http://www.ghostproducerforhire.com/",
          image: require("../assets/ghostproducer.jpg"),
          tags: ["Bootstrap", "jQuery"]
        }
      ]
    };
  }
};
</script>

<style>
h1 {
    margin-bottom: 3rem;
}
h3 {
  text-align: justify;
}
.mediaImage {
  max-width: 470px;
  margin: auto;
}
.projects {
  margin-top: 2rem;
}
</style>
