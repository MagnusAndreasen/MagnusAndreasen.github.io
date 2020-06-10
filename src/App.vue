<template>
  <div id="app">
    <Navbar />
    <Users />
    <Footer />
  </div>
</template>

<script>
import Navbar from './Navbar';
import Users from './Users';
import Footer from './Footer';

export default {
  name: "App",
  components: {
    Navbar,
    Users,
    Footer
  },
  data() {
    return {
      
    };
  },
  methods: {
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
h1 {
  text-align: center;
}
</style>
