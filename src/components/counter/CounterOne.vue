<script setup>

import { onMounted, ref, onUpdated } from 'vue'

import axios from "axios";

const counter = ref([]);

onMounted(async () => {
  const { data: fetchedCounter } = await axios.get("/data/counter.json");
  counter.value = fetchedCounter.counter;
});

onUpdated(() => {     
    $(".counter-number span").counterUp({
		delay: 10,
		time: 1000,

	});
  
});

</script>


<template>
    <div class="achievement-area">
 		  <h2 class="title">¡Regístrate ahora y dale un nuevo enfoque a tu negocio!</h2> 
 	</div>
</template> 

<style scoped>


@media (max-width: 767px) {
	.title{
	font-size: 18px;
	position: absolute;
  text-align: center;
    top: 230px;
    left: 10px;
	color: #ffffff;
	
}
}
@media (min-width: 768px) {
.title{
	font-size: 30px;
	position: absolute;
  text-align: center;
    top: 230px;
    left: 200px;
	color: #ffffff;
}
}
</style>