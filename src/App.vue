<template>
  <h1 class="name">Plate number</h1> {{ car.plateNumber }}
  <h2 class="name2">Hourse power</h2> <p> {{ car.hoursepower }} </p>

  <span v-if="iscoolCar(car)"> Ahujenna </span>
  <span v-if="isbadCar(car)"> Leta masina </span>
</template>

<script>
export default {
  data () {
    return {
      car: {
        plateNumber: "AA-3333",
        hoursepower: 1200,
        price: 77,
      }
    }
  },
  methods: {
    iscoolCar (car) {
      console.log(car)
      return (car.hoursepower > 1000)
    },
    isbadCar (car2) {
      return (car2.price < 3000 )
    }
  }
}
</script>

<style>
  .name {
    color:red;
  }
  .name2 {
    color:blue;
  }
  p {
    color:pink;
  }
</style>
