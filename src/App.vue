<template>
  <div id="app">
	<Home />
	<Menu />
	<About />
	<Events />
  </div>
</template>

<script>
import Home from './components/Home.vue'; 
import Menu from './components/Menu.vue';
import About from './components/About.vue';
import Events from './components/Events.vue';

export default {
  name: 'App',
  components: {
    Home,
	Menu,
	About,
	Events
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&family=Raleway&family=Satisfy&display=swap');

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
  overflow: hidden; 
}

.main {
	margin: 0px 200px 0px 200px; 
}

p {
	font-family: 'Raleway', sans-serif;
}


</style>
