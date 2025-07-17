<template>
  <div id="app">
    <!-- Conditionally render components -->
 
    
    <UI
      v-if="situation === 'HomeScreen'"
      @craft="handleCraft"
      @map="handleMapClick"
      @base="handleBaseClick"
      @production="handleProductionClick"
      @next-phase="handleNextPhase"
    />
    
    <WorldMap
      :base-position="basePosition"
      @drag="handleMapDrag"
    />
  </div>
</template>

<script>
import UI from './UI.vue'
import WorldMap from './WorldMap.vue'

export default {
  components: {
    UI,
    WorldMap
  },
  data() {
    return {
      phase: 'day',
      situation: 'HomeScreen', // Initialize situation
      basePosition: { x: 0, y: 0 }, // Initialize basePosition
      resources: { 
        supplies: 20, 
        fuel: 10, 
        scrap: 15
      },
      mapData: [] // Your map data here
    }
  },
  methods: {
    handleTravel(coords) {
      // Update position logic
    },
    handleCraft(recipe) {
      // Crafting logic
    },
    handleDefense(action) {
      // Defense logic
    },
    handleMapClick() {
      // Map button logic
    },
    handleBaseClick() {
      // Base button logic
    },
    handleProductionClick() {
      // Production button logic
    },
    handleNextPhase() {
      // Next phase logic
    },
    handleMapDrag(event) {
      // Map drag logic
    }
  }
}
</script>

<style scoped>
/* Your styles here */
</style>