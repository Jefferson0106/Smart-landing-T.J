<script setup>

import { onMounted, ref} from 'vue'

import axios from "axios";

const features = ref([]);

onMounted(async () => {
  const { data: fetchedFeatures } = await axios.get("/data/features.json");
  features.value = fetchedFeatures.features;
});


</script> 

<template>
    <div class="about-area section-padding">
 		<div class="container">
 			<div class="row align-items-center">
 				<div class="col-lg-6 col-md-12 col-sm-12">
					<div class="about-img-wrap">
                    <div class="image-one wow fadeInUp" data-wow-delay=".2s" style="visibility: visible; animation-delay: 0.2s; animation-name: fadeInUp;">
                        <img class="imagen-cel" src="/assets/img/bank-card-mobile-phone-online-payment.jpg" alt="">
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
 							<h2 class="h2-titulo"><span class="punto"></span>Automatiza procesos de pago</h2>
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
</template>


<style scoped>
 @media (max-width: 767px) {
	h1{
	top: -60px;
	left: -10px;
	margin: 60px;
	text-align: center;
	font-size: 19px;
	white-space: nowrap;
	color: #006fff;
}
.h2-titulo{
	top: -80px;
	left: -10px;
	color: #006fff;
	display: flex;
        align-items: center;
		font-size: 20px;
	margin: 1px;
	white-space: nowrap;
	
	
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
		top: -50px;
		left: 60px;
		width: 30%;
		top: 90px;
		margin: 20px;
		margin: 60px;
		position: absolute;
	}
	p{
	margin: 1px;
	top: -70px;
	left: 10px;
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
	left: -90px;
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
		width: 65%;
	}
p{
	margin: 4px;
	left: -46px;
	color: #313131;
}
 }
</style>