<script>
import axios from 'axios';
import { toast } from 'vue3-toastify';
import 'vue3-toastify/dist/index.css';

export default {
  name: "NuevoQsd",
  data: function() {
    return {
      ID: null,
      form: {
        id: "",
        nombre: "",
        correo: "",
        telefono: "",
        nombreEmpresa: "",
        mensaje: "",
        Token: "",
      }
    };
  },
  methods: {
    registrar() {
      this.form.Token = localStorage.getItem("Token");
      axios.post("https://smartsalesagent-api.azurewebsites.net/SmartBotForWhatsApp/Registro", this.form)
        .then(data => {
          console.log(data);
          // Mostrar notificación de éxito
          toast.success("¡Registro creado con éxito!", {
            autoClose: 3000,
          });
          this.$router.push("/");
        })
        .catch(error => {
          console.error(error);
          // Mostrar notificación de error
          toast.error("Hubo un error al crear el registro.", {
            autoClose: 3000,
          });
        });
    },
  }
};
</script>


<template>
	<div class="project-bg">
	 <div class="container">
	 <form>
			 <input type="text" class="form-control mb-2" id="inlineFormInput" placeholder="Nombre completo:" v-model="form.nombre" required>
			 <input type="text" class="form-control" id="inlineFormInputGroup" placeholder="Correo electrónico" v-model="form.correo" required>
			 <input type="text" class="form-control mb-2" id="inlineFormInput" placeholder="Teléfono:" v-model="form.telefono" required>
			 <input type="text" class="form-control mb-2" id="inlineFormInput" placeholder="Empresa:" v-model="form.nombreEmpresa" required>
			 <textarea id="mensaje" name="mensaje" rows="4" placeholder="Mensaje (opcional):" v-model="form.mensaje" required></textarea>
			 
			 <button type="button" @click="registrar">COMIENZA AHORA</button>
		 </form>
		 <!-- Modal -->
		 <div v-if="showModal" class="modal">
        <div class="modal-content">
          <p>{{ modalMessage }}</p>
          <button @click="accept" class="modal-button accept-button">Aceptar</button>
          <button @click="cancel" class="modal-button cancel-button">Cancelar</button>
        </div>
      </div>
 </div>
	</div>
 </template>
 
 <style scoped>
 
 @media (max-width: 767px) {
	.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal-content {
  background-color: blue;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.modal-button {
  margin: 0 10px;
  padding: 8px 16px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.accept-button {
  background-color: #4caf50;
  color: #fff;
}

.cancel-button {
  background-color: #f44336;
  color: #fff;
}
	 .container {
			 max-width: 10px; /* Ajusta el ancho máximo según tus preferencias */
			 margin: 0 auto;
			 padding: 20px;
			 background-color: #f9f9f9;
			 border-radius: 10px;
		 }
		 input, textarea, button {
			 width: 100%;
			 padding: 50px;
			 color: #000;
			 margin-bottom: 15px;
			 border: 1px solid #ccc;
			 border-radius: 5px;
		 }
		 button {
			 background-color: #007BFF;
			 color: #fff;
			 cursor: pointer;
		 }
 }

 
 
   .container {
			 max-width: 1200px; /* Ajusta el ancho máximo según tus preferencias */
			 margin: 0 auto;
			 padding: 20px;
			 background-color: #f9f9f9;
			 border-radius: 10px;
		 }
		 input, textarea, button {
			 width: 100%;
			 padding: 10px;
			 color: #000;
			 margin-bottom: 15px;
			 border: 1px solid #ccc;
			 border-radius: 5px;
		 }
		 button {
			 text-align: center;
			 width:45% ;
			 background-color: #fff;
			 color: #000;
			 cursor: pointer;
			 display: block;
			 margin: 0 auto;
			 border: 2px solid #006fff; /* Borde azul de 2px */
		 }

		 .modal-content {
  background-color: blue;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.modal-button {
  margin: 0 10px;
  padding: 8px 16px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.accept-button {
  background-color: #4caf50;
  color: #fff;
}

.cancel-button {
  background-color: #f44336;
  color: #fff;
}
		
 </style>