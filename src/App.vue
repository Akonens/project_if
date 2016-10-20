<template>
  <div class="color" v-if="user.isAdmin">
    Es esmu admins
    <strong>{{user.name}}</strong>
    <button @click="logout()">Logout</button>
  </div>
  <div v-if="!user.isAdmin">
    Es esmu parasts lietotajs

    <input v-model="user.name">
    <input type="password" v-model="user.pass">

    <button @click="authorize(user.name, user.pass)">Log In</button>
  </div>
</template>
<script>
export default {
  data () {
    return {
      user: {
        name: "",
        pass: "",
        isAdmin: false,
      },
    }
  },
  methods: {
    authorize (username, password)  {
      if(username == "admin" && password == "z") {
        this.user.isAdmin = true
      } else {
        this.user.pass = ""
      }
    },
    logout () {
      this.user.isAdmin = false
    }
  }
}
</script>

<style>
.color {

}

</style>
