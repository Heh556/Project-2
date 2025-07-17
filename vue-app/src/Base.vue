<template>
  <div class="base-ui">
    <!-- Resource Display -->
    <div>
      <div>
        <span class="resource-amount">{{ resources.supplies }}</span>
      </div>
      <div>
        <span class="resource-amount">{{ resources.electricity }}</span>
      </div>
      <div>
        <span class="resource-amount">{{ resources.materials }}</span>
      </div>
    </div>

    <!-- Function Buttons -->
    <div class="function-buttons">
      <button v-for="n in 6" class="fn-button" @click="$emit('f' + n)">
        F{{ n }}
      </button>
    </div>

    <!-- Action Buttons -->
    <div class="action-buttons">
      <button @click="$emit('back')" class="action-button">Back</button>
      <button @click="$emit('manage')" class="action-button">Manage</button>
      <button @click="$emit('production')" class="action-button">Production</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BaseUI',
  props: {
    resources: {
      default: () => ({
        supplies: 0,
        electricity: 0,
        materials: 0
      })
    }
  },
  emits: ['back', 'manage', 'production', 'f1', 'f2', 'f3', 'f4', 'f5', 'f6']
}
</script>

<style scoped>

</style>