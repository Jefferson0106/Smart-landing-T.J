<script setup>

import { onMounted } from 'vue'

onMounted(() => {     

	$('.homepage-slides').owlCarousel({
		items: 1,
		dots: false,
		nav: true,
		loop: true,
		autoplay: true,
		autoplayTimeout: 5000,
		smartSpeed: 2000,
		slideSpeed: 600,
		animateOut: 'fadeOut',
		navText: ["<i class='la la-angle-left'></i>", "<i class='la la-angle-right'></i>"],
		responsive: {
			0: {
				items: 1,
				nav: false,
				dots: false,
			},
			600: {
				items: 1,
				nav: false,
				dots: false,
			},
			768: {
				items: 1,
				nav: false,
				dots: false,
			},
			1100: {
				items: 1,
				nav: true,
				dots: false,
			}
		}
	});


	$(".homepage-slides").on("translate.owl.carousel", function () {
		$(".single-slide-item h1").removeClass("animated fadeInUp").css("opacity", "1");
		$(".single-slide-item h6").removeClass("animated fadeInDown").css("opacity", "1");
		$(".single-slide-item p").removeClass("animated fadeInDown").css("opacity", "1");
		$(".single-slide-item a.main-btn").removeClass("animated fadeInDown").css("opacity", "1");
	});

	$(".homepage-slides").on("translated.owl.carousel", function () {
		$(".single-slide-item h1").addClass("animated fadeInUp").css("opacity", "1");
		$(".single-slide-item h6").addClass("animated fadeInDown").css("opacity", "1");
		$(".single-slide-item p").addClass("animated fadeInDown").css("opacity", "1");
		$(".single-slide-item a.main-btn").addClass("animated fadeInDown").css("opacity", "1");
	});
  
});

</script>

<template>
    <div >
 		<div class="single-slide-item">
 			<div class="overlay"></div>
 			<div class="hero-area-content">
 				<div class="container">
 					<div class="row justify-content-center">
 						<div class="col-lg-12 wow fadeInUp animated" data-wow-delay=".2s">
 							<div class="section-title">
 								<!-----h6 class="text-white">We Build only big things</h6> --->
 								<h1>IMPULSA TUS VENTAS<br></h1>
								<h3>lleva tu negocio al siguiente nivel</h3>
 								<p>Descubre cómo nuestra solución de atención al cliente multi-empresa puede <br>transformar la forma en que gestionas tus productos, servicios y clientes.<br> Con Smart Sales, maximiza la eficiencia y mejora la experiencia de tus clientes  <br>con herramientas avanzadas de automatización e integración.</p>
								 <button class="boton-registro">contactanos </button>
								 <img class="robot-registro"  src="/assets/img/Floating-Robot.png" alt="" >
								
 							</div>
							
 							<!---router-link :to="{name:'about'}" class="main-btn">Learn More</router-link>----->
 						</div>
 					</div>
 				</div>
 			</div>
 		</div>

 		<!---div class="single-slide-item hero-area-bg-2">
 			<div class="overlay"></div>
 			<div class="hero-area-content">
 				<div class="container">
 					<div class="row justify-content-center">
 						<div class="col-lg-12 wow fadeInUp animated" data-wow-delay=".2s">
 							<div class="section-title">
 								<h6 class="text-white">We provide best satisfied work</h6>
 								<h1>We turn vision<br> Factory Solutions</h1>
 								<p> Industrial Revolution, in modern history, the process of change from an agrarian <br>and handicraft economy to one dominated by industry and machine manufacturing.</p>
 							</div>
 							<router-link :to="{name:'about'}" class="main-btn">Learn More</router-link>
 						</div>
 					</div>
 				</div> 
 			</div>
 		</div>---->
 	</div> 
</template>

<style scoped>
@media (max-width: 767px) {
	.boton-registro {
	background: #ffffff;
	color: #646464;
	font-size: 16px;
	padding: 10px 40px;
	text-align: center;
	vertical-align: middle;
	cursor: pointer;
	border: 2px solid #006fff; /* Borde azul de 2px */
}
.robot-registro{
	width: 55%;
    position: absolute;
    top: -150px;
    left: 80px;
}
}


@media (min-width: 768px) {
	.robot-registro{
	width: 39%;
	position: absolute;
	top: -90px;
	left: 700px;
}
.boton-registro {
	background: #ffffff;
	color: #646464;
	font-size: 16px;
	padding: 10px 40px;
	text-align: center;
	vertical-align: middle;
	cursor: pointer;
	border: 2px solid #006fff; /* Borde azul de 2px */
}
}
</style>
