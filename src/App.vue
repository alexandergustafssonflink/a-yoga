<template>
  <div id="app">
	<Home />
	<Menu />
	<MobileMenu />
	<About :teachers="teachers" :about="about" /> 
	<Offer />
	<!-- <Events /> -->
	<Footer />
  </div>
</template>

<script>
import Home from './components/Home.vue'; 
import Menu from './components/Menu.vue';
import MobileMenu from './components/MobileMenu.vue';
import About from './components/About.vue';
// import Events from './components/Events.vue';
import Offer from './components/Offer.vue';
import Footer from './components/Footer.vue';
import AOS from 'aos';
import client from "@/contentful.js";
import 'aos/dist/aos.css'; 
// ..
AOS.init();

export default {
  name: 'App',
  components: {
    Home,
	Menu,
	MobileMenu,
	About,
	Offer,
	// Events,
	Footer
  },
  data() {
    return {
    teachers: [
	],
	about: ""
    };
  },
  mounted() {
    client
      .getEntries({
        content_type: "sections",
      }).then((entries) => { 
		this.teachers = entries.items.filter(e => e.fields.type == "teacher");
		this.about = entries.items.filter(e => e.fields.type == "om" )
})
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&family=Raleway&family=Satisfy&display=swap');
@import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css'); 


* {
	padding: 0; 
	margin: 0; 
}


#app {
  font-family: 'Montserrat', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  --purple: #501B38; 
  --beige: #EDD7CA; 
  --darkbeige: #D3B19D; 
  overflow-x: hidden; 
}

.main {
	margin: 0px 10% 0px 10%; 
}

p {
	font-family: 'Raleway', sans-serif;
}


@media only screen and (max-width: 600px) {
  .main {
    margin: 0px 15px 0px 15px; 
  }
}


@media only screen and (min-width: 600px) and (max-width: 800px) {
  .main {
	margin: 0px 50px 0px 50px;  
  }
}
</style>
