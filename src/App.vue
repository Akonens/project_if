<template>
  <input type="text" v-model="username"> <br>
  <input type="text"> <br>
  {{username.length}}
  <div v-if="username.lenght">
    Saulit debesis spiid
  </div>
</template>

<script>
export default {
  data () {
    return {
      username: ""
    }
  }
}
submit () {
  if(this.username == "suka") {
    alert(fuck off)
  }
}



</script>

<style>

</style>
