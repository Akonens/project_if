<template>
  <ul>

    <li v-for="item in menu"
        v-bind:class="{active: item.active}"
        @click="goToPage(item)">
      {{ item.title }}
    </li>
  </ul>


</template>

<script>
export default {
  data () {
    return {
      menu: [
        {
          title: "Home",
          active: true,
        },
        {
          title: "Contats",
          active: false,
        },
      ]
    }
  },
  methods: {
    goToPage (menuitem) {
      for (let i in this.menu)
      {
        this.menu[i].active = false
      }
      menuitem.active = true
    }
  }
}

</script>

<style>
  .active {
    color:red;
  }
</style>
