<template>
  <div class="ui-container">
    <!-- Bottom Action Bar -->
    <div class="action-bar">
      <button 
        class="action-button"
        @click="$emit('map')"
      >

        <span class="label">Map</span>
      </button>

      <button 
        class="action-button"
        @click="$emit('base')"
      >

        <span class="label">Base</span>
      </button>

      <button 
        class="action-button"
        @click="$emit('production')"
      >

        <span class="label">Production</span>
      </button>

      <button 
        class="action-button next-phase"
        @click="$emit('next-phase')"
      >

        <span class="label">Next Phase</span>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'UI',
  emits: ['map', 'base', 'production', 'next-phase', 'craft']
}
</script>

<style scoped>

</style>

