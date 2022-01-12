<template>
<section id="about">
<img class="mandala-top" src="@/assets/mandala.png" alt="">
<div class="main">
	<div class="upper">
		<div class="inner-upper">
			<div class="img-wrapper"><img src="@/assets/ocean-pose.jpg" alt="ocean pose"></div>
			<div data-aos="fade-left" class="about-text">
				<h1>{{about[0].fields.header}}</h1>
				<RichTextRenderer :document="about[0].fields.text" />
				<a href="#contact"><button>Kontakta oss</button></a>
			</div>
		</div>
	</div>
	<img class="mandala-middle" src="@/assets/mandala.png" alt="mandala">
	<div class="lower">
		<div class="teacher-info" v-for="teacher in teachers"  :key="teacher.fields.header">
			<div class="img-wrapper" data-aos="zoom-in">
				<img :src="teacher.fields.image.fields.file.url" alt="">
			</div>
			<h1>{{teacher.fields.header}}</h1>
			<RichTextRenderer :document="teacher.fields.text" />
		</div>
	
	</div>
	<img class="mandala-bottom" src="@/assets/mandala.png" alt="mandala">
</div>

</section>
</template>

<script>
import { documentToHtmlString } from '@contentful/rich-text-html-renderer';
import RichTextRenderer from 'contentful-rich-text-vue-renderer';

export default {
	components: {
   RichTextRenderer
  },
  name: 'About',
	props: ["about", "teachers"],
	methods: {
    formatContent(content) {
		console.log(content);
		let html = documentToHtmlString(content)
		return html
    },
	formatHtml() {
		let richTextFields = document.querySelectorAll(".rich-text")
		console.log(richTextFields);
		richTextFields.forEach(f => f.innerHTML = "hej")
	}
  },
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#about {
	background-color: var(--beige); 
	position: relative; 
	padding-bottom: 100px; 
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
	/* height: 100%;  */
	/* display: flex;
	justify-content: center;  */
}
.upper .img-wrapper {
	width: 600px; 
	height: 600px; 
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
	width: 90%; 
	padding: 30px; 
	text-align: left;
	top: 7%;
	left: 68%; 
	box-shadow: rgba(0, 0, 0, 0.16) 0px 3px 6px, rgba(0, 0, 0, 0.23) 0px 3px 6px;
}

.about-text a {
	color: white; 
	
}
.about-text button {
    color: var(--beige); 
	background-color: var(--purple); 
    border: 2px solid var(--beige); 
    padding: 10px 15px;  
	margin-top: 20px; 
    font-size: 1em; 
    transition: 0.3s ease;
}

.about-text button:hover {
    border: 2px solid var(--purple); 
    background-color: var(--beige); 
	color: var(--purple);  
}

.about-text p {
	margin-bottom: 12px; 
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
	min-height: 730px; 
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
	bottom: -6%; 
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
	padding-bottom: 50px; 
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
	bottom: -2%; 
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

@media only screen and (min-width: 800px) and (max-width: 1300px) {
	.teacher-info {
width: 300px; 	
}
}
</style>