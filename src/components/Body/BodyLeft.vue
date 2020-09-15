<template>
  <div>


    <div v-on:click="firstRoutes"
         v-if="memory.firstRoutesBool">
      {{ memory.name }}
    </div>

    <div v-else>
      <Routes
          v-bind:memory="memory"
      />
    </div>

  </div>

</template>

<script>

import Routes from "@/components/Body/Routes/RouterPerents/Routes";

export default {
  name: "BodyLeft",
  components: {Routes},
  props: ['memory'],
  methods: {
    firstRoutes() {
      this.memory.firstRoutesBool = false
    }
  }

}

</script>

<style>

</style>