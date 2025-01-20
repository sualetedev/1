<template>
    <div>
        <img :src="require('@/assets/foto.png')" alt="foto" id="imagen">
    </div>
    <div id="total">
        <h1 class="text-primary">Carta de presentación</h1>
        <p class="text-muted">Mi nombre es {{ miNombre }} {{ Izquierdo }} y actualmente estudio {{ DAW }} aunque también tengo el titulo de {{ estudios }}.
            Lo que más me gusta es el front-end, aunque también he tocado lenguajes de programación como Java y Python.
        </p>
        <p class="text-muted">Tras 8 años de experiencia laboral en sectores industriales, he decidido dar un cambio significativo en mi vida y volver a estudiar. He elegido el Desarrollo de Aplicaciones Web (DAW), y la experiencia hasta ahora ha sido increíblemente gratificante y enriquecedora.

He estudiado lenguajes como Java, C#, JavaScript, PHP, así como otros lenguajes de marcas como CSS y HTML. y finalmente me enamoré de Python y Django, ampliando así mi conocimiento y habilidades en el desarrollo de aplicaciones modernas y escalables.

Además, manejo bases de datos relacionales, usando programas como SQL y SQL Developer, tambien tengo experiencia en bases de datos no relacionales como MongoDB. Esta combinación de conocimientos me permite diseñar y gestionar sistemas de datos eficientes y robustos.

Soy una persona constante y trabajadora, con una sólida ética de trabajo y una pasión por aprender y mejorar continuamente. Mi trayectoria profesional me ha dotado de habilidades técnicas y prácticas, y ahora estoy ansioso por aplicar este nuevo conocimiento en el campo del desarrollo web.</p>
        
    </div>
    <div>
        <p>
            <button class="btn btn-primary" v-on:click="link()">Linkedin</button>
            <button class="btn btn-primary" v-on:click="link2()">Github</button>
        </p>
    </div>
</template>

<script>
export default {
    data(){
        return{
            miNombre: "Alejandro",
            miApellido: "Izquierdo",
            estudioActual: "DAW",
            estudios: "ASIR , SEA"
        };
    },
    methods:{
        link(){
            window.location.href = "https://www.linkedin.com/in/alejandro-izquierdo-garcia-8333a9114/";
        },
        link2(){
            window.location.href = "https://github.com/sualetedev";
        },

    },
}
</script>

<style>
    #total{
        margin-left: 5%;
        margin-right: 5%;
    }
    #imagen{
        height: 10%;
        width: 10%;
    }
</style>