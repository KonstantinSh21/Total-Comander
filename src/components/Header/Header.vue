<template>
  <div>
    <span v-if="memory.firstRoutesBool === false">
      {{memory.name}}
    </span>
    <span
        v-if="memory.routes[0].secondRoutesBool === false">
      {{memory.routes[0].name}}
    </span>
  </div>
</template>

<script>

export default {
  name: 'Header',
  props: [
      'memory'
  ]
}


</script>

<style>

</style>