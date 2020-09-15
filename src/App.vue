<template>
  <div class="wrapper">
    <div class="wrapper-item">

      <div class="wrapper-header">
        <Header
            v-bind:memory="discOne"
        />
      </div>

      <div class="wrapper-bogy">

        <div class="wrapper-bogy__component">
          <BodyLeft
              :memory="discOne"
          />
        </div>

        <div class="wrapper-bogy__component">
          <BodyRight/>
        </div>

      </div>
    </div>
  </div>
</template>


<script>


import Header from "@/components/Header/Header";
import BodyLeft from "@/components/Body/BodyLeft";
import BodyRight from "@/components/Body/BodyRight";


export default {
  name: 'App',

  // mounted() {
  //   fetch('@/components/memory.json')
  //       .then((data) =>{console.log(JSON.stringify(data))})
  //
  // },


  data() {
    return {

      discOne: {
        //routes first
        firstRoutesBool: true,
        name: "D:",
        id: "1",
        routes: [
          {
            name: "Cats",
            id: "1.1",
            secondRoutesBool: true,
            routes: [
              {
                name: "Catone",
                id: "2.1",
              }, {
                name: "Cattwo",
                id: "2.2",
              }, {
                name: "Catthree",
                id: "2.3",
              }
            ]
          }, {
            name: "Cars",
            id: "1.2"
          }, {
            name: "Music",
            id: "1.3"
          }
        ]
      },


    }
  },
  components: {
    Header,
    BodyLeft,
    BodyRight
  }
}
</script>

<style>
.wrapper {
  width: 50%;
  margin: 0 auto;
  padding: 0 32px 0 32px;
}

.wrapper-item {
  background-color: #ccc;
  min-height: 400px;
}

.wrapper-header {
  width: 100%;
  height: 30px;
  background-color: #ddd;
}

.wrapper-bogy {
  background-color: #999;
  min-height: 100%;
  display: flex;
}

.wrapper-bogy__component {
  flex: 1 1 50%;
  border: 1px solid #000;
  min-height: 370px;

}


</style>
