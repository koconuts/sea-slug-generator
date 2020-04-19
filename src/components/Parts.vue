<template>
  <div>
    <div class="selector-heading-container">
      <h2 class="text selector-heading">頭触手</h2>
    </div>
    <shape-selector></shape-selector>
    <color-selector></color-selector>
    <!-- <div class="selector-heading-container">
      <h2 class="text selector-heading">二次鰓</h2>
    </div> -->
  </div>
</template>

<script>
import ShapeSelector from '../components/ShapeSelector.vue';
import ColorSelector from '../components/ColorSelector.vue';

export default {
  name: 'Parts',
  components: {
    ShapeSelector,
    ColorSelector,
  },
}
</script>
