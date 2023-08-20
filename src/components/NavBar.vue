<template>
  <div>
    <nav class="d-flex justify-space-between pa-3">
      <div class="d-flex">
        <a href="/">
          <img
            src="https://car-rental-ten.vercel.app/static/media/logo.0ad964cb93ab30cc809d.png"
            alt=""
            width="100px"
          />
        </a>
      </div>
      <div>
        <ul class="d-flex">
          <li class="d-flex px-5 cursor">Inicio</li>
          <li class="d-flex px-5 cursor">Vehículos</li>
          <li class="d-flex px-5 cursor">Contacto</li>
        </ul>
      </div>
      <div>
        <a href="">Registrar</a>
        <a href="">Loguear</a>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "navbar-comp",
  created() {},
  data() {
    return {};
  },
  props: {},
  methods: {},
};
</script>

<style scoped>
.cursor {
  cursor: pointer;
}
.cursor:hover {
  color: rgb(164, 6, 6);
}
</style>
