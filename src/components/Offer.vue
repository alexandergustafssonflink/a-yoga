<template>
<section id="offer">
	<div class="main">
		<div class="offer-info">
			<h1>Vi erbjuder</h1>
			<h3>Terminsabonnemang (vår eller höst) med 2 pass i veckan.</h3>
			<p><span>Måndagar 18.30-19.30: </span> Härlig Hatha Yoga med Isabel <br>
			<span>Torsdagar 18.30-19.30:</span> Lugn & avstressande Yin Yoga med Lottie <br><br> Klasserna anpassas efter eleverna med personlig coaching och massor av extramaterial.<br><br> Terminstart 6e september.<br> En termin med 28 klasser kostar 2000 kr. <br>Två terminer med 56 klasser kostar 3000 kr. <br><br> Kontakta oss för att pröva en vecka gratis på Ahderinne Yoga på <a href="kontakt@a-yoga.se">kontakt@a-yoga.se</a></p>
			<h3>Sommarklasser utomhus i fantastisk havsmiljö och slottsmiljö.</h3>
			<p>Varma klippor och ljudet av vågor på Femöre. Kontakta oss för mer info eller varför inte prenumerera på vårt nyhetsbrev som bara skickas 3 ggr per år.<br> <a href="mailto:kontakt@a-yoga.se"> Klicka här </a> och skriv “nyhetsbrev” i mailet.</p>
		</div>
		<div data-aos="fade-left" class="img-wrapper">
			<img src="@/assets/meditation.jpg" alt="">
		</div>
	</div>
	<img class="lotus-colored" src="@/assets/lotus-colored.svg" alt="">
</section>
</template>

<script>

export default {
  name: "Offer",
 
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#offer {
  padding-bottom: 100px; 
  width: 100vw; 
  background-color: #F6F5F3; 
  position: relative; 
}

.main {
	padding-top: 100px; 
	z-index: 2; 
	position: relative; 
	display: flex;
	justify-content: space-between;
}


.offer-info {
	width: 45%; 
}

.offer-info a {
	color: inherit; 
	text-decoration: none;
	font-weight: 700; 
}

.offer-info span {
	font-weight: 700; 
}

.main h1 {
	text-align: left;
	color: var(--purple)
}
.main .img-wrapper {
	width: 45%; 
	height: 60vh; 
	box-shadow: rgba(0, 0, 0, 0.25) 0px 14px 28px, rgba(0, 0, 0, 0.22) 0px 10px 10px;
}

.main h3 {
	text-align: left;
	color: var(--purple); 
	margin-top: 30px;
}

.main h5 {
	color: #C97C42;
	font-weight: 400; 
	margin-bottom: 10px; 
}


.main p {
	text-align: left;
	margin-top: 12px; 
}


.img-wrapper img {
	width: 100%; 
	height: 100%; 
	object-fit: cover;
}

.event-card button {
	border: none; 
	background: none;
	text-align: right;
	color: var(--purple); 
	width: 63px; 
	align-self: flex-end;
	display: flex;
	align-items: center;
	justify-content: space-between; 
	padding: 5px 0px; 

}

.event-info {
	padding: 20px; 
	height: 100%; 
	display: flex;
	flex-direction: column;
	justify-content: space-between;
}

.lotus-colored {
	position: absolute;
	bottom: -22%; 
	left: 41%; 
	/* z-index: 10 */
	}


@media only screen and (max-width: 800px) { 
	.main {
		padding-top: 50px; 
		flex-direction: column;
	}

	.offer-info {
		width: 100%; 
	}

	.main .img-wrapper {
		width: 100%; 
		margin-top: 20px; 
}

	.lotus-colored {
		width: 50%; 
		bottom: -10%; 
		left: 70%; 
	}
}

@media only screen and (min-width: 600px) and (max-width: 800px) {
	.events-list {
		align-items: flex-start;
		margin-top: 30px; 
	}
}
</style>