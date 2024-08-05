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
	<div class="project-bg">
		<div class="h1-mensaje1">
    Lorem ipsum dolor sit amet?
    <div class="dropdown">
        <span class="arrow">▼</span>
        <div class="dropdown-content">
            <a href="#">Opción 1</a>
            <a href="#">Opción 2</a>
            <a href="#">Opción 3</a>
        </div>
    </div>
</div>
	</div>
 </template>
 
 <style scoped>
.h1-mensaje1 {
    position: relative;
    width: 70%;
    top: -210px;
    left: 130px;
    padding: 20px;
    color: #000;
    background-color: aliceblue;
}

.dropdown {
    position: relative;
    cursor: pointer;
}

.arrow {
    font-size: 18px;
    margin-right: 10px;
}

.dropdown-content {
    display: none;
    position: absolute;
    background-color: #f9f9f9;
    min-width: 160px; /* Ajusta según sea necesario */
    box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
    top: 100%; /* Despliega hacia abajo */
    left: 0; /* Alinea con el borde izquierdo */
}

.dropdown-content a {
    color: black;
    padding: 12px 16px; /* Ajusta según sea necesario */
    text-decoration: none;
}

.dropdown:hover .dropdown-content {
    display: block;
}
 </style>
 