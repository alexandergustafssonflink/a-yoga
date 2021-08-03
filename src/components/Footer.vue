<template>
<footer id="contact">
	<div class="contact">
		<h1>Kontakt</h1>
		<p><a href="mailto:namaste@a-yoga.se">mail: namaste@a-yoga.se</a>   </p>
		<p>tel: 0733 - 44 11 11</p>
	</div>
	<div class="logo-wrapper">
		<img class="logo" src="@/assets/logo-transparent.png" alt="">
	</div>
</footer>
</template>

<script>
export default {
  name: 'Footer',
  props: {
    // msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

footer {
	height: 200px; 
	padding: 50px 200px; 
	display: flex; 
	justify-content: space-between;
}

.contact {
	text-align: left;
	color: var(--purple)
}

h1 {
	margin-bottom: 10px; 
}
.logo {
	height: 60px; 
}

a {
	text-decoration: none;
	color: var(--purple); 
}
p {
	color: var(--purple); 
}

@media only screen and (max-width: 800px) {
  footer {
    padding: 15px; 
	flex-direction: column;
  }

  .logo-wrapper {
	text-align: left; 
  }
}


@media only screen and (min-width: 600px) and (max-width: 800px) {
	footer {
    padding: 50px; 
}
	.lotus-colored {
		bottom: -13%;
	}
}


</style>