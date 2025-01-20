<template>
  <p id="primer">Hola mundo usando componentes y variables:</p>
  <p id="segundo">Mi nombre es {{ nombre }} y mis apellido {{ apellido }} y tengo {{ edad }} años</p>
  <p id="tercer"> Esta es mi primera página usando Vue.js</p>
  <br><br><br><br>
</template>

<script>
export default {
  data(){
   return{
    nombre: "Alejandro",
    apellido: "Izquierdo",
    edad: 32,
   }
  }

}
</script>

<style>
  #primer {color:red; 
   font-size:20px;
   font-family:Courier;
   font-weight:bold;
   font-style:italic;
   line-height:30px;
   letter-spacing:5px;
   text-decoration:underline;
   text-transform:capitalize;
   text-align:left;
   text-indent:30px;
  }
  #segundo {color:rgb(111, 0, 255); 
   font-size:10px;
   font-family:Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
   font-style:italic;
   font-size: 40px;
   line-height:30px;
   letter-spacing:5px;
   text-align:left;
   text-indent:30px;
  }
  #tercer {color:rgb(0, 0, 0); 
   font-size:10px;
   font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
   font-style:italic;
   font-size: 40px;
   line-height:30px;
   letter-spacing:5px;
   text-align:left;
   text-indent:30px;
  }
</style>