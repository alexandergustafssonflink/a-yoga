<template>
<section id="events">
	<div class="main">
		<h1>Events</h1>
		<div class="events-list">
			<div class="event-card">
				<div class="img-wrapper">
					<img src="@/assets/siluett.jpg" alt="">
				</div>
				<div class="event-info">
					<h3>Yoga grejer</h3>
					<h5>24e juni kl 18:00</h5>
					<p>There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form.</p>
					<button>Mer info</button>
				</div>
			</div>
		</div>
	</div>
</section>
</template>

<script>
export default {
  name: 'Events',
  props: {
    // msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#events {
  height: 90vh; 
  width: 100vw; 
  background-color: #F6F5F3; 
}

.main {
	padding-top: 100px; 
}

.main h3 {
	text-align: left;
	color: var(--purple)
}

.main h5 {
	color: #C97C42;
	font-weight: 400; 
	margin-bottom: 10px; 
}

.event-card {
	width: 300px; 
	height: 400px; 
	background: var(--beige);
	text-align: left;
	box-shadow: rgba(60, 64, 67, 0.3) 0px 1px 2px 0px, rgba(60, 64, 67, 0.15) 0px 2px 6px 2px;
}

.event-card .img-wrapper {
	width: 100%; 
	height: 150px; 
}

.img-wrapper img {
	width: 100%; 
	height: 100%; 
	object-fit: cover;
}

.event-card button {
	float: right;
	float:inline-end
}

.event-info {
	padding: 20px; 
}

</style>