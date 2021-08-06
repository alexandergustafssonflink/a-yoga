<template>
<section id="events">
	<div class="main">
		<h1>Events</h1>
		<div class="events-list">
			<div v-for="event in events" :key="event.title" class="event-card" data-aos="fade-up">
				<div class="img-wrapper">
					<img :src="event.fields.image.fields.file.url" alt="">
				</div>
				<div class="event-info">
					<div class="event-info-inner"> 
						
						<h3>{{event.fields.title}}</h3>
						<h5>{{event.fields.date}}</h5>
						<p>{{event.fields.shortDescription}}</p>
					</div>
					<button>Mer info <i class="fas fa-chevron-right"></i></button>
				</div>
			</div>
		</div>
	</div>
	<img class="lotus-colored" src="@/assets/lotus-colored.svg" alt="">
</section>
</template>

<script>

import client from "@/contentful.js";


	client
      .getEntries({
        content_type: "event",
      }).then((entries) => {
	return entries.items; 
})

export default {
  name: "Events",
  data() {
    return {
      events: [],
    };
  },
  mounted() {
    client
      .getEntries({
        content_type: "event",
      }).then((entries) => {
	this.events = entries.items;
})
  },
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#events {
  padding-bottom: 100px; 
  width: 100vw; 
  background-color: #F6F5F3; 
  position: relative;
}

.main {
	padding-top: 100px; 
	z-index: 2; 
	position: relative; 
}

.main h1 {
	text-align: left;
	color: var(--purple)
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

.events-list {
	display: flex;
	margin: 50px -30px 0px -30px; 
	justify-content: space-between;
	flex-wrap: wrap;
	/* position: relative;
	z-index: 2000;  */
}
.event-card {
	width: 300px; 
	height: 400px; 
	background: var(--beige);
	margin: 30px; 
	text-align: left;
	box-shadow: rgba(60, 64, 67, 0.3) 0px 1px 2px 0px, rgba(60, 64, 67, 0.15) 0px 2px 6px 2px;
	display: flex;
	flex-direction: column;
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
	bottom: -20%; 
	left: 41%; 
	/* z-index: 10 */
	}


@media only screen and (max-width: 800px) { 

	#events  {
		height: auto; 
	}
	.events-list {
		flex-direction: column; 
		margin-top: 20px; 
		align-items: center;
		padding-bottom: 20px; 
	}

	.main {
		padding-top: 50px; 
	}

	.event-card {
		margin: 0px 0px 20px 0px; 
		width: auto; 
		max-width: 400px;
	}

	.lotus-colored {
		width: 50%; 
		bottom: -7%; 
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