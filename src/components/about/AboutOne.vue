<template>
    <div class="about-area section-padding">
 		<div class="container">
			<h1>¿Qué puedes hacer con Smart Sales?</h1>
 			<div class="row align-items-center">
 				<div class="col-lg-6 col-md-12 col-sm-12">
					<div class="about-img-wrap">
                    <div class="image-one wow fadeInUp" data-wow-delay=".2s" style="visibility: visible; animation-delay: 0.2s; animation-name: fadeInUp;">
                        <img class="imagen-cel" src="/assets/img/whatsapp.png" alt="">
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
 							<h2 class="h2-titulo"><span class="punto"></span>Interacción automática</h2>
 						</div>
 						<p>Optimiza la comunicación con tus clientes mediante nuestro chatbot inteligente, integrado con WhatsApp y potenciado por GPT-4. Responde automáticamente a consultas frecuentes, muestra catálogos y ayuda a tus clientes a realizar pedidos o reservas de citas sin complicaciones.</p>
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
	left: -55px;
	margin: 60px;
	text-align: center;
	font-size: 15px;
	white-space: nowrap;
	color: #006fff;
}
.h2-titulo{
	top: -190px;
	left: -10px;
	color: #006fff;
	display: flex;
        align-items: center;
		font-size: 18px;
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
		left: 90px;
		width: 30%;
		top: 150px;
		margin: 20px;
		margin: 10px;
		position: absolute;
	}
	p{
	margin: 4px;
	top: -190px;
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
		position: absolute;
		left: 70px;
		top: -130px;
		width: 55%;
	}
p{
	margin: 4px;
	left: -46px;
	color: #313131;
}
 }
</style>