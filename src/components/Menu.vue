<template>
<nav>
	<ul class="menu-options">
		<li><a href="#home">Hem</a> </li>
		<li><a href="#about">Om</a>	</li>
		<li><a href="#offer">Vi erbjuder</a> </li>
		<li><a href="#contact">Kontakt</a> </li>
	</ul>
	<div>
		<img class="logo" src="@/assets/logo-transparent.png" alt="">
	</div>
</nav>
</template>

<script>
export default {
  name: 'Menu',
  props: {
    // msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
nav {
	position: fixed;
	z-index: 1000;
	top: 0px; 
	height: 50px;
	width: 100%; 
	display: flex; 
	justify-content: space-between;
	align-items: center; 
	background-color: rgba(255, 255, 255, 0.2);
	box-shadow: rgba(60, 64, 67, 0.3) 0px 1px 2px 0px, rgba(60, 64, 67, 0.15) 0px 2px 6px 2px;
}

ul {
	list-style-type: none;
	display: flex; 
	justify-content: space-between;
	margin-left: 200px; 
	width: 30%; 
}

a {
	text-decoration: none;
	color: var(--purple); 
	transition: 0.3s ease;
}

li {
	font-weight: 600; 
	color: #501B38; 
	
}

a:hover {
	color: var(--darkbeige); 
}


.logo {
	height: 50px; 
	margin-right: 50px; 
}


@media only screen and (max-width: 800px) {
  nav {
    display: none; 
  }
}

</style>