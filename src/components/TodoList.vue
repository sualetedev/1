<template>
  <p id="formulario">Formulario: </p>
    <div id="formulario">
        <form @submit.prevent="submitForm">
            <div>
                <label for="nombre">Nombre: </label>
                <input type="text" id="name" v-model="form.name" />
                <span v-if="errors.name" class="error">{{ error.name }} </span>
            </div>

            <div>
                <label for="correo">Correo electrónico: </label>
                <input type="email" id="email" v-model="form.email" />
                <span v-if="errors.email" class="error">{{ error.email }} </span>
            </div>

            <button type="submit">Enviar </button>
        </form>
    </div>

</template>
  
<script>
  export default {
    data() {
    return {
      form: {
        name: '',
        email: '',
        password: '',
      },
      errors: {
        name: null,
        email: null,
        password: null,
      },
    };
  },
  methods: {
    validateForm() {
      this.errors = {}; // Reiniciar errores
      let valid = true;

      if (!this.form.name) {
        this.errors.name = 'El nombre es obligatorio.';
        valid = false;
      }

      if (!this.form.email) {
        this.errors.email = 'El correo electrónico es obligatorio.';
        valid = false;
      } else if (!/\S+@\S+\.\S+/.test(this.form.email)) {
        this.errors.email = 'El correo electrónico no es válido.';
        valid = false;
      }

      if (!this.form.password) {
        this.errors.password = 'La contraseña es obligatoria.';
        valid = false;
      } else if (this.form.password.length < 6) {
        this.errors.password = 'La contraseña debe tener al menos 6 caracteres.';
        valid = false;
      }

      return valid;
    },
    submitForm() {
      if (this.validateForm()) {
        alert('Formulario enviado con éxito');
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