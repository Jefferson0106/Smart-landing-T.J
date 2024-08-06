<script>
import { onMounted, ref } from "vue";
import axios from "axios";

export default {
  name: "TestimonialCarousel",
  setup() {
    const testimonials = ref([]);

    onMounted(async () => {
      try {
        const { data } = await axios.get("/data/testimonials.json");
        testimonials.value = data.testimonials;
      } catch (error) {
        console.error("Error fetching testimonials:", error);
      }
    });

    return {
      testimonials,
    };
  },
};
</script>


<template>
  <div>
    <h1>Nuestros Planes</h1>
<div class="container">
  <div class="card">
    <h2>Prueba</h2>
    <div class="price">15<span>/Días Gratis</span></div>
    <ul>
      <li>o	Prueba todas las funcionalidades de Smart Sales sin ningún costo durante 15 días.</li>
      <li>o	Acceso completo a la integración con GPT-4 y WhatsApp.</li>
      <li>o	Gestión de productos y servicios.</li>
      <li>o	Automatización de órdenes y pagos.</li>
      <li>o	Soporte básico incluido.</li>
     
    </ul>
    <button>SELECT PLAN</button>
  </div>
  <div class="card">
    <h2>Básico </h2>
    <div class="price">$50<span>/mes</span></div>
    <ul>
      <li>o	Hasta 5000 mensajes al mes.</li>
      <li>o	Integración con GPT-4 y WhatsApp.</li>
      <li>o	Gestión completa de productos y servicios.</li>
      <li>o	Automatización de órdenes y pagos.</li>
      <li>o	Soporte por email.</li>
      <li>o	Almacenamiento de conversaciones y datos de contacto.</li>
    </ul>
    <button>SELECT PLAN</button>
  </div>
  <div class="card" style="background-color: #dce9ee;">
    <h2>Avanzado </h2>
    <div class="price">$80<span>/mes</span></div>
    <ul>
      <li>o	Hasta 10000 mensajes al mes.</li>
      <li>o	Todas las funcionalidades del Plan Básico.</li>
      <li>o	Soporte prioritario.</li>
      <li>o	Reportes avanzados y analíticas de uso.</li>
      <li>o	Integración personalizada con la base de datos de productos.</li>
   
    </ul>
    <button>SELECT PLAN</button>
  </div>
  <!---div class="card">
    <h2>Ultra</h2>
    <div class="price">$99<span>/MONTH</span></div>
    <ul>
      <li>100GB Linux Web Space</li>
      <li>Unlimited MySQL Databases</li>
      <li>Unlimited Email</li>
      <li>10000Gb mo Transfer</li>
      <li>24/7 Tech Support</li>
      <li>Daily Backups</li>
    </ul>
    <button>SELECT PLAN</button>
  </div> --->
</div>
</div>
 </template>
 
 <style scoped>

@media (max-width: 767px) {
  .container {
 
  gap: 10px;
}
h1{
  text-align: center;
  white-space: nowrap;
  color: #006fff;
  font-size: 35px;
  margin: 40px;
}

.card {
  background-color: #dce9ee;
  border-radius: 10px;
  padding: 30px;
  text-align: center;
  width: 320px;
}

.card h2 {
  margin-bottom: 20px;
  font-size: 24px;
}

.card p {
  margin-bottom: 10px;
}

.card ul {
  list-style-type: none;
  padding: 0;
}

.card ul li {
  margin-bottom: 5px;
  font-size: 14px;
}

.card .price {
  font-size: 48px;
  font-weight: bold;
  margin-bottom: 20px;
}

.card .price span {
  font-size: 14px;
  font-weight: normal;
}

.card button {
  background-color: #006fff;
  color: #fff;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  font-size: 16px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.card button:hover {
  background-color: #0056b3;
}
}


@media (min-width: 768px) {

.container {
  display: flex;
  gap: 190px;
}
h1{
  text-align: center;
  white-space: nowrap;
  color: #006fff;
  font-size: 50px;
  margin: 40px;
}

.card {
  background-color: #dce9ee;
  border-radius: 10px;
  padding: 30px;
  text-align: center;
  width: 250px;
}

.card h2 {
  margin-bottom: 20px;
  font-size: 24px;
}

.card p {
  margin-bottom: 10px;
}

.card ul {
  list-style-type: none;
  padding: 0;
}

.card ul li {
  margin-bottom: 5px;
  font-size: 14px;
}

.card .price {
  font-size: 48px;
  font-weight: bold;
  margin-bottom: 20px;
}

.card .price span {
  font-size: 14px;
  font-weight: normal;
}

.card button {
  background-color: #006fff;
  color: #fff;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  font-size: 16px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.card button:hover {
  background-color: #0056b3;
}
}
 </style>
 