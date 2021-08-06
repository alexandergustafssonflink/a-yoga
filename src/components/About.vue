<template>
<section id="about">
<img class="mandala-top" src="@/assets/mandala.png" alt="">
<div class="main">
	<div class="upper">
		<div class="inner-upper">
			<div class="img-wrapper"><img src="@/assets/island.png" alt=""></div>
			<div data-aos="fade-left" class="about-text">
				<h1>Om oss</h1>
				<p>It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout. The point of using Lorem Ipsum is that it has a more-or-less normal distribution of letters, as opposed to using 'Content here, content here', making it look like readable English. Many desktop publishing packages and web page editors now use Lorem Ipsum as their default model text, and a search for 'lorem ipsum' will uncover many web sites still in their infancy.</p>
				<a href="#contact"><button>Kontakta oss</button></a>
			</div>
		</div>
	</div>
	<img class="mandala-middle" src="@/assets/mandala.png" alt="">
	<div class="lower">
		<div class="teacher-info">
			<div class="img-wrapper" data-aos="zoom-in">
				<img src="@/assets/examensbevis.jpg" alt="">
			</div>
			<h1>Isabel Ahderinne</h1>
			<p>There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour, or randomised words which don't look even slightly believable. If you are going to use a passage of Lorem Ipsum, you need to be sure there isn't anything embarrassing hidden in the middle of text. </p>
		</div>
		<div class="teacher-info">
			<div class="img-wrapper" data-aos="zoom-in">
				<img src="@/assets/header-v2.jpg" alt="">
			</div>
			<h1>Lottie Ahderinne</h1>
			<p>There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour, or randomised words which don't look even slightly believable. If you are going to use a passage of Lorem Ipsum, you need to be sure there isn't anything embarrassing hidden in the middle of text. </p>
		</div>
	</div>
	<img class="mandala-bottom" src="@/assets/mandala.png" alt="">
</div>

</section>
</template>

<script>
export default {
  name: 'About',
  props: {
    // msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#about {
	height: 180vh; 
	background-color: var(--beige); 
	position: relative; 
	/* overflow-x: hidden;  */
}

.mandala-top {
	position: absolute; 
	top: -120px; 
	left: -100px; 
	width: 400px;
	z-index: 1
}

.mandala-middle {
	position: absolute;
	top: 31%; 
	right: -9%; 
	width: 600px; 
	z-index: 1;
}

.main {
	height: 100%; 
	/* display: flex;
	justify-content: center;  */
}
.upper .img-wrapper {
	width: 30vw; 
	height: 30vw; 
	box-shadow: rgba(0, 0, 0, 0.16) 0px 3px 6px, rgba(0, 0, 0, 0.23) 0px 3px 6px;
}

.img-wrapper img {
	width: 100%; 
	height: 100%; 
	object-fit: cover;
	right: 30%; 
}

.about-text {
	background: var(--purple);
	color: white; 
	position: absolute; 
	width: 100%; 
	padding: 30px; 
	text-align: left;
	top: 12%;
	left: 70%; 
	box-shadow: rgba(0, 0, 0, 0.16) 0px 3px 6px, rgba(0, 0, 0, 0.23) 0px 3px 6px;
}

.about-text button {
	border: none;
	padding: 10px 15px;  
	background-color: var(--beige); 
	color: var(--purple); 
	margin-top: 20px; 
}

.about-text h1 {
	margin-bottom: 12px; 
}

.inner-upper {
	position: relative;
	right: 16%; 
	margin-top: 100px; 
}
.upper {
		display: flex;
	justify-content: center; 
	z-index: 2; 
	position: relative;
}

.lower {
	display: flex;
	justify-content: space-around;
	margin-top: 100px; 
}

.teacher-info {
	width: 400px; 
	height: 600px; 
	background: #F6F5F3;
	display: flex;
	flex-direction: column;
	align-items: center;
	padding: 30px;
	position: relative;
	z-index: 2;
	box-shadow: rgba(0, 0, 0, 0.16) 0px 3px 6px, rgba(0, 0, 0, 0.23) 0px 3px 6px;
	
}

.teacher-info .img-wrapper {
	width:300px;
	height: 300px; 
	border-radius: 50%;
}

.lower .img-wrapper img {
	width: 100%;
	height: 100%;
	object-fit: cover;
	border-radius: 50%;
} 

.teacher-info h1 {
	color: var(--darkbeige); 
	margin: 20px; 
}

.mandala-bottom {
	position: absolute;
	bottom: -8%; 
	left: -10%; 
	width: 500px; 
	z-index: 1; 
}

button:hover {
	cursor: pointer;
}

@media only screen and (max-width: 800px) {
  #about {
    height: auto; 
  }

  .upper .img-wrapper {
	width: 100%;
	height: 300px; 
	display: none; 
  }


  .inner-upper {
	right: 0%; 
	margin-top: 0px; 
  }

.about-text {
	position: relative; 
	width: auto; 
	padding: 15px; 
	text-align: center; 
	top: 0%; 
	left: 0%; 
	margin-top: 50px; 
}

.mandala-top {
	width: 250px; 
}

.mandala-middle {
	width: 300px; 
	top: 21%; 
}

.lower {
	margin-top: 50px; 
	flex-direction: column;
}

.teacher-info {
	width: auto; 
	margin-bottom: 15px; 
	padding: 30px 10px;  
	height: auto; 
}

.mandala-bottom {
	width: 300px; 
	bottom: -3%; 
	left: -15%; 
}
}

@media only screen and (min-width: 600px) and (max-width: 800px) {
	.teacher-info {
	padding: 50px 30px; 
	margin-bottom: 50px; 
}
	#about  {
		padding-bottom: 70px; 
	}
}
</style>