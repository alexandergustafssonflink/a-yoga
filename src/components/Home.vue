<template>
<section id="home">
	<div class="header-container">
		<img class="header-img" src="@/assets/header-with-logo-min.jpg" alt="header image with logo">
		<!-- <img class="logo" src="@/assets/logo-transparent.png" alt=""> -->
		<img class="linear-border" src="@/assets/linear-header.png" alt="linear">
	</div>
	<div class="main">
		<div class="upper">
			<img class="olive-branch" src="@/assets/olive-branch-left.svg" alt="olive branch">
			<div class="description">
				<h1>Yogaklasser för dig<br> som du är <br> för att nå ditt mål</h1>
				<img src="@/assets/lotus-side.png" alt="lotus">
			</div>
			<img class="olive-branch" src="@/assets/olive-branch.svg" alt="olive branch">
		</div>
		<div class="lower">
			<div data-aos="fade-up" class="img-wrapper"><img src="@/assets/yoga-mat-purple-min.jpg" alt="yoga mat"></div>
			<div data-aos="fade-up" class="img-wrapper"><img src="@/assets/lotus-on-cliff-min.png" alt="lotus pose on cliff"></div>
			<div data-aos="fade-up" class="img-wrapper"><img src="@/assets/back-with-shadow-min.jpg" alt="girl with shadow"></div>
		</div>
	</div>
</section>
</template>

<script>
export default {
  name: 'Home',
  props: {
    // msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#home {
  height: 190vh; 
  width: 100vw; 
  background-color: #F6F5F3; 
}

#home .logo {
	display: none; 
}

.header-container {
	width: 100%; 
	height: 100vh; 
	position: relative; 
}

.linear-border {
	position: absolute;
	bottom: 0px; 
	left: 0px;
	width: 100%; 
}

.header-img {
	width: 100%; 
	height: 100%; 
	object-fit: cover;
}

.main {
	display: flex;
	justify-content: center;
	align-items: center;
	flex-direction: column;
	height: 90vh; 
}

.upper {
	display: flex; 
	justify-content: space-between; 
	width: 100%; 
}

.description {
	position: relative; 
	align-items: center; 
}


.description h1 {
	position: absolute;
	top: 50%;
	left: 50%;
	transform: translate(-50%, -50%);
	font-family: 'Satisfy';
	color: var(--purple); 
	font-size: 36px; 
}

.olive-branch {
	width: 200px; 
}

.lower {
	display: flex; 
	justify-content: space-between; 
	margin-top: 50px; 
	width: 100%; 
	z-index: 2; 
	padding-bottom: 50px; 
}

.img-wrapper {
	width: 32%; 
	height: 250px; 
	box-shadow: rgba(0, 0, 0, 0.16) 0px 3px 6px, rgba(0, 0, 0, 0.23) 0px 3px 6px;
}

.img-wrapper img {
	width: 100%; 
	height: 100%; 
	object-fit: cover;
}


@media only screen and (max-width: 600px) {
	#home {
		height: auto; 
	}

	.description h1 {
		font-size: 30px; 
	}

	.header-container {
		height: 60vh; 
		position: relative
	}

	#home .logo {
		display: block;
		position: absolute;  
		top: 15%; 
		left: 33%; 
}
	.upper {
		width: auto; 
	}
	.main {
		height: auto; 
	}
	.lower {
		flex-direction: column;
		margin-top: 15px; 
	}

	.lower .img-wrapper {
		width: 100%; 
		margin-bottom: 15px; 
	}

}

@media only screen and (min-width: 600px) and (max-width: 800px) {
	#home {
		height: auto; 
		padding-bottom: 100px; 
	}
  .upper {
	width: auto; 
	margin-top: 50px; 
  }

  .main {
	height: auto; 
  }

  .olive-branch {
	display: none; 
  }
}
</style>