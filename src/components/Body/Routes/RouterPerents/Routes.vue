<template>
  <div>

    <div class="f"
         v-if="memory.routes[0].secondRoutesBool">
      <div class="s">
        <span v-on:click="secondRoutes">
          {{ memory.routes[0].name }}
        </span>
        <span>
          {{ memory.routes[1].name }}
        </span>
        <span>
          {{ memory.routes[2].name }}
        </span>


      </div>
      <div class="s" v-on:click="firstRoutes">
        Стрелка
      </div>

    </div>

    <div v-else>
      <Cat v-bind:memory="memory" />
    </div>


  </div>


</template>

<script>
import Cat from "@/components/Body/Routes/RouterChildren/Cat";

export default {
  name: "Routes",
  components: {Cat},
  props: ['memory'],
  methods: {
    secondRoutes() {
      this.memory.routes[0].secondRoutesBool = false
    },
    firstRoutes() {
      this.memory.firstRoutesBool = true
    }
  }
}
</script>

<style>
.f {
  display: flex;
}

.s {
  flex: 1 1 50%;
}
</style>