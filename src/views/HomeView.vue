<template>
  <main>
    <section class="d-flex">
      <div>
        <h5>Planea tu viaje ahora!</h5>
        <h1>
          Ahorra <span style="color: red">mucho</span> con nuestro servicio de
          rent car!
        </h1>
        <p>
          Arrienda el auto que siempre has querido. Precios imbatibles,
          kilómetros ilimitados, flexibilidad de recogida y mucho más!
        </p>
        <div class="d-flex">
          <v-btn>Agenda tu vehículo</v-btn>
          <v-btn>Más información</v-btn>
        </div>
      </div>
      <div>
        <img
          src="https://car-rental-ten.vercel.app/static/media/main-car.9b30faa59387879fa060.png"
          alt=""
        />
      </div>
    </section>
    <section>
      <BookCar />
    </section>
  </main>
</template>

<script>
import BookCar from "@/components/BookCar.vue";
export default {
  name: "Home-view",

  components: {
    BookCar,
  },
};
</script>
