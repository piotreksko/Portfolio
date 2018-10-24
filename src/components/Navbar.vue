<template>
  <v-toolbar dark>
    <v-toolbar-title v-html="appName" />
    <v-spacer />

    <v-btn icon href="https://www.linkedin.com/in/piotr-skorupa-731856156/" target="_blank" right>
      <img :src="imageLinkedIn" height="32" />
    </v-btn>

    <v-btn icon href="https://github.com/piotreksko" target="_blank" right>
      <img :src="imageGithub" height="32" />
    </v-btn>

  </v-toolbar>
</template>

<script>
export default {
  name: "Navbar",
  data () {
    return {
    }
  },
  props: {
    appName: {
      type: String,
      default: ''
    },
    folderImage: {
      type: String,
      default: ''
    }
  },
  computed: {
    imageLinkedIn () {
      return this.folderImage + 'icon-linkedin-34.png';
    },
    imageGithub () {
      return this.folderImage + 'icon-github-32.png';
    }
  },

};



</script>

