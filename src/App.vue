<template>
  <div id="app">
    <Header/>
    <Main :postCategories="categories"/>
    <Footer :postCategories="categories"/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  },
  data: function(){
    return {
      categories :[
        "GADGETS",
        "PHOTOGRAPHY",
        "LIFESTYLE",
        "FASHION",
        "RECIPES",
        "TRAVEL",
        "BUSINESS",
        "ARCHITECTURE",
        "REVIEWS",
        "SPORTS",
        "VIDEOS",
        "TECHNOLOGY",
        "DESIGN"
      ]
    }
  }
}
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
@import "@/style/main-style.scss";
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

#app {
  font-family: 'Montserrat', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

</style>
