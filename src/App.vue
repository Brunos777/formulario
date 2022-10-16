  <template>
  <div class="container mt-3">
    <div class="row">
      <div class='col-12 col-md-4'>
    <h1> App- Proyectos </h1>
    </div>
    <img width="100" :src="url" alt="des">
      </div>
    </div>
    <hr/>



   <form @submit.prevent="addUser">
    <div>
    <label>
      Nombre:
    <input v-model="nombre" type="text" placeholder="Nombre"  required /> </label></div>
 
  <div><label>
      Edad:
    <input  v-model="edad"  type="number" min="1" max="80" placeholder="Edad" required /> </label>
  </div>
  <div>
    <label>
      Correo:
    <input  v-model="correo"  type="email" placeholder="email@mail.com"  required /> </label>
  </div>

    <button type="submit">Enviar</button>

</form>
</template>

<script>
export default {
  data: () => ({
    url: "https://cdn.svgporn.com/logos/vue.svg",
    des: "Vue.js",
    nombre: "",
    edad: 0,
    correo:"",
  }),
  methods: {
    adduser() {
      console.log(this.nombre, this.edad, this.correo);
    },
  },
};
</script>