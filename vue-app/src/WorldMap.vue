<template>
  <div 
    class="map-container"
    @mousedown="startDrag"
    @mousemove="handleDrag"
    @mouseup="stopDrag"
  >
    <img 
    img 
    />
    <!-- mark base -->
   
  </div>
</template>

<script>
export default {
  props: ['basePosition'],
  data() {
    return {
      //position and etc
    };
  },
  methods: {
        //handledrag
  }
};
</script>

<style scoped>

</style>


