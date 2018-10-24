<template>
  <v-app>
    <Navbar :app-name="appName" :folder-image="folderImage" />
    <Header />
    <Projects />
    <Contact />
    <Footer />
  </v-app>
</template>

<script>
import Navbar from '@/components/Navbar';
import Header from '@/components/Header';
import Projects from '@/components/Projects';
import Contact from '@/components/Contact';
import Footer from '@/components/Footer';

export default {
  name: 'App',
  components: {
    Navbar,
    Footer,
    Header,
    Projects,
    Contact
  },
  data () {
    return {
      appName: "Portfolio of Piotr Skorupa",
      folderImage:'https://raw.githubusercontent.com/ijklim/portfolio/gh-pages/assets/img/'
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Quicksand');

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  font-family: 'Quicksand', sans-serif;
}
</style>
