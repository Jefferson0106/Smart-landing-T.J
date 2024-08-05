<script setup>

import { onMounted, ref, onUpdated } from 'vue'

import axios from "axios";

const services = ref([]);

onMounted(async () => {
  const { data: fetchedServices } = await axios.get("/data/services.json");
  services.value = fetchedServices.services;
});

onUpdated(() => {     

		// Service Slider    
        $(".service-slider").owlCarousel({
		loop: true,
		items: 3,
		dots: true,
		nav: false,
		smartSpeed: 1000,
		autoHeight: false,
		touchDrag: true,
		mouseDrag: true,
		margin: 30,
		autoplay: true,
		slideSpeed: 600,
		responsive: {
			0: {
				items: 1,
				nav: false,
				dots: false,
			},
			600: {
				items: 2,
				nav: false,
				dots: false,
			},
			768: {
				items: 2,
				nav: false,
				dots: false,
			},
			1100: {
				items: 3,
				nav: false,
				dots: true,
			}
		}
	});
  
});

</script>

<template>
   <div>
	<div class="about-area section-padding">
 		<div class="container">
			
 			<div class="row align-items-center">
 				<div class="col-lg-6 col-md-12 col-sm-12">
					<div class="about-img-wrap">
                    <div class="image-one wow fadeInUp" data-wow-delay=".2s" style="visibility: visible; animation-delay: 0.2s; animation-name: fadeInUp;">
						<h2 class="h2-titulo"><span class="punto"></span>Gestiona tus productos y servicios</h2>
                    </div>                        
                    <div class="image-two wow fadeInUp" data-wow-delay=".4s" style="visibility: visible; animation-delay: 0.4s; animation-name: fadeInUp;">
                        <!---img src="/assets/img/about/about-page-2.jpg" alt=""> --->
                    </div>                                            
                </div> 					
 				</div>
 				<div class="col-lg-6 col-md-12 col-sm-12">
 					<div class="info-content-area">
 						<div class="section-title">
 							<!---h6>About Us</h6> --->
							 <img class="imagen-cel" src="/assets/img/boxes2.png" alt="">
 						</div>
 						<p>We are build construction site lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea enim et, similique minus soluta ipsum dolor sit, amet consectetur adipisicing elit.</p>
 						<!---div class="about-list-item mt-30">
							<p class="highlight">Since our launch in 1995, to deliver high value project.</p>
							<p class="highlight">We always provide flexible & quality task. </p>
							<p class="highlight">Uninque latest machinary used the industrial project.</p>
						</div>

 						<div class="row founded">
 							<div class="col-lg-4 col-md-6 col-12">
 								<div class="years"><span>25</span>Year of Success</div>
 							</div>
 							<div class="col-lg-8 col-md-6 col-12">
 								<div class="text">Since we established in 1995 experience &amp; still a growing protfolio day by day!</div>
 							</div>
 						</div> --->
 					</div>
 				</div>

 			</div>
 		</div>
 	</div>
	</div>
</template>


<style scoped>
 @media (max-width: 767px) {
	h1{
	top: -60px;
	left: -80px;
	margin: 60px;
	text-align: center;
	font-size: 19px;
	white-space: nowrap;
	color: #006fff;
}
.h2-titulo{
	top: -160px;
	left: 20px;
	color: #006fff;
	display: flex;
        align-items: center;
		font-size: 18px;
	margin: 1px;
	
}
.punto {
        width: 19px;
        height: 15px;
        background-color: #006fff;
        border-radius: 50%;
        margin-right: 10px;
    }
	.section-title h2 {
		display: table-cell;
	}
	.imagen-cel{
		width: 85%;
		top: 10px;
		margin: 20px;
		position: absolute;
	}
	p{
	margin: 4px;
	top: -170px;
	color: #313131;
}
 }


 @media (min-width: 768px) {
h1{
	top: -60px;
	left: -30px;
	margin: 60px;
	text-align: center;
	font-size: 45px;
	color: #006fff;
}
.h2-titulo{
	top: -80px;
	left: 40px;
	color: #006fff;
	display: flex;
        align-items: center;
		font-size: 30px;
	margin: 1px;
	white-space: nowrap;
}
.punto {
        width: 20px;
        height: 20px;
        background-color: #006fff;
        border-radius: 50%;
        margin-right: 10px;
    }
	.section-title h2 {
		display: inline;
	}
	.imagen-cel{
		position: absolute;
		top: -200px;
		width: 85%;
	}
p{
	margin: 4px;
	left: -606px;
	color: #313131;
}
 }
</style>

