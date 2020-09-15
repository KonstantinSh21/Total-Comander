<template>
  <div>
<div>
  <div>
    <span>{{memory.routes[0].routes[0].name}}.jpg   </span>
    <span>{{memory.routes[0].routes[1].name}}.jpg   </span>
    <span>{{memory.routes[0].routes[2].name}}.jpg</span>
  </div>

  <div v-on:click="secondRoutes">
    Стрелка
  </div>
</div>

  </div>
</template>

<script>

export default {
  name: 'Cat',
  props: [
    'memory'
  ],
  methods:{
    secondRoutes() {
      this.memory.routes[0].secondRoutesBool = true
    },

  }
}


</script>

<style>

</style>