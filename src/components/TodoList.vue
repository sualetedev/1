<template>
  <p id="formulario">Formulario: </p>
    <div id="formulario">
        <form @submit.prevent="submitForm">
            <div>
                <label for="tarea">Tarea: </label>
                <input type="text" id="name" v-model="inputValue"/>
                <span v-if="errors.tarea" class="error">{{ error.tarea }} </span>
            </div>
            <button type="submit">Enviar </button>
        </form>
    </div>
    <div id="formulario"> 
      <p> Tareas agregadas: </p>
      <ul>
        <li v-for="(tarea, index) in tareas" :key="index"> {{ tarea }} </li>
      </ul>
    </div>

</template>
  
<script>
  export default {
    data() {
    return {
      inputValue: "",
      tareas: [],
      form: {
        tarea: '',    
      },
      errors: {
        tarea: null,
      },
    };
  },
  methods: {
    validateForm() {
      this.errors = {}; // Reiniciar errores
      let valid = true;

      if (!this.inputValue) {
        this.errors.tarea = 'Tienes que introducir una tarea';
        valid = false;
      }
      return valid;
    },
    submitForm() {
      if (this.validateForm()) {
        //Introducir el valor del submit en la variable
        this.tareas.push(this.inputValue);
        //Resetear input a ""
        this.inputValue= "",
        console.log(this.form);
      }
    },
  },
}
</script>
  
<style>
#formulario {
  color: black;
  font-size: 30px;
  font-family: Courier;
  text-align: Left;  
}
.error {
  color: red;
  font-size: 0.9em;
}
</style>