<template>
<nav class="mobile-menu">
	<div class="hamburger-menu" @click="mobileSliderOpen = !mobileSliderOpen" >
		<img alt="sitting yoga pose" src="@/assets/sitting-pose.svg" class="hamburger" :class="mobileSliderOpen ? 'hide' : 'show'">
		<img alt="cross yoga pose" src="@/assets/cross-pose.svg" class="hamburger cross" :class="mobileSliderOpen ? 'show' : 'hide'">
	</div>
	<div class="mobile-slider" :class="mobileSliderOpen ? 'active' : ''">
		<ul class="menu-options" @click="mobileSliderOpen = false">
			<li><a href="#home">Hem</a> </li>
			<li><a href="#about">Om</a>	</li>
			<li><a href="#offer">Vi erbjuder</a> </li>
			<li><a href="#contact">Kontakt</a> </li>
		</ul>
	</div>
</nav>
</template>

<script>
export default {
  name: 'MobileMenu',
  props: {
    // msg: String
  },
  data() {
    return {
      mobileSliderOpen: false
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
nav {
	width: 100vw; 
}

.hamburger-menu {
	position: fixed; 
	top: 20px; 
	right: 20px; 
	z-index: 5000; 
	width: 40px;
	height: 40px; 
}


.cross {
	position: relative;
	bottom: 45px; 
}
.hamburger-menu img {
	width: 100%; 
	height: 100%; 
}
.mobile-slider {
	position: fixed; 
	background: #FFEFD6; 
	height: 100vh; 
	width: 100vw; 
	z-index: 1000; 
	top: 0px; 
	right: -100vw; 
	transition: 0.3s ease; 
}


.menu-options {
	text-align: left; 
	margin-top: 100px; 
	margin-left: 30px; 
}
.hamburger {
	transition: 0.3s ease;
}
.hamburger.hide{
	transform: scale(0%)
}

.hamburger.show{
	transform: scale(100%)
}


.mobile-slider.active {
	top: 0px; 
	right: 0px; 
}

ul {
	list-style-type: none;
}

li {
	padding: 10px; 
	font-weight: 700; 
	font-size: 20px; 
}

a {
	text-decoration: none;
	color: var(--purple); 
	transition: 0.3s ease;
	padding: 10px; 
}



@media only screen and (min-width: 800px) {
  nav {
    display: none; 
  }
}

</style>