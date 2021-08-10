<template>
<footer id="contact">
	<div class="contact">
		<h1>Kontakt</h1>
		<p><a href="mailto:namaste@a-yoga.se"><i class="fas fa-envelope"></i> kontakt@a-yoga.se</a>   </p>
		<p><i class="fas fa-phone"></i> 0730 777 046 & 0766 447 721</p>
		<a class="facebook" href="https://www.facebook.com/ahderinneyoga"><p><i class="fab fa-facebook"></i> Ahderinne Yoga</p></a>
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

<style scoped>

footer {
	height: 230px; 
	padding: 50px 200px; 
	display: flex; 
	justify-content: space-between;
}

.contact {
	text-align: left;
	color: var(--purple)
}

h1 {
	margin-bottom: 15px; 
}
.logo {
	height: 60px; 
}

a {
	text-decoration: none;
	color: var(--purple); 
		display: flex; 
	align-items: center;
}
p {
	color: var(--purple); 
	margin-top: 12px; 
	display: flex; 
	align-items: center;
}

footer .fab {
	font-size: 26px; 
	margin-right: 5px; 
}

footer .fas {
	font-size: 26px; 
	margin-right: 5px; 
}

@media only screen and (max-width: 800px) {
  footer {
    padding: 15px; 
	height: 270px; 
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