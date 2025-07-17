<template>
  <div id="app">
    
    
    <!--Phase -->
    <MapView 
      v-if="phase === 'day'" 
      :locations="mapData" 

    />
    <UI 
      v-if="phase === 'day'"
      @craft="handleCraft"

    />
    <WorldMap 
    :base-position="basePosition" 
    @drag = "HandleMapDrag"
    />
    <!-- https://learnvue.co/articles/vue-drag-and-drop @drag-->

  </div>
</template>

<script>
export default {
  data() {
    return {
        
      resources: { supplies: 20, fuel: 10, scrap: 15},
      mapData: [ /* data */ ]
    };
  },
  methods: {
    handleTravel(coords) { /* Update position */ },
    handleCraft(recipe) { /* Deduct resources */ },
    handleDefense(action) {}
  }
};
</script>

<sytle scoped>

</sytle>
