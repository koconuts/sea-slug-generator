<template>
  <div>
    <div class="selector-heading-container">
      <h2 class="text selector-heading">せなか</h2>
    </div>
    <shape-selector
      :shapeSelectorItems="shapeSelectorItemsSurface"
      :name="surface"
    ></shape-selector>
    <color-selector
      :colorSelectorItems="colorSelectorItemsSurface"
      :name="surfaceColor"
    ></color-selector>
    <div class="selector-heading-container">
      <h2 class="text selector-heading">ふち</h2>
    </div>
    <color-selector
      :colorSelectorItems="colorSelectorItemsSide"
      :name="sideColor"
    ></color-selector>
  </div>
</template>

<script>
import ShapeSelector from '../components/ShapeSelector.vue';
import ColorSelector from '../components/ColorSelector.vue';

export default {
  name: 'Design',
  components: {
    ShapeSelector,
    ColorSelector,
  },
  data() {
    return {
      surface: 'surface',
      surfaceColor: 'surfaceColor',
      sideColor: 'sideColor',
      shapeSelectorItemsSurface: [
        {id: 'radio_img_surface1'},
        {id: 'radio_img_surface2'},
        {id: 'radio_img_surface3'},
        {id: 'radio_img_surface4'}
      ],
      colorSelectorItemsSurface: [
        {id: 'radio_color_surface1'},
        {id: 'radio_color_surface2'},
        {id: 'radio_color_surface3'},
        {id: 'radio_color_surface4'},
        {id: 'radio_color_surface5'},
        {id: 'radio_color_surface6'},
        {id: 'radio_color_surface7'},
        {id: 'radio_color_surface8'},
        {id: 'radio_color_surface9'},
        {id: 'radio_color_surface10'}
      ],
      colorSelectorItemsSide: [
        {id: 'radio_color_side1'},
        {id: 'radio_color_side2'},
        {id: 'radio_color_side3'},
        {id: 'radio_color_side4'},
        {id: 'radio_color_side5'},
        {id: 'radio_color_side6'},
        {id: 'radio_color_side7'},
        {id: 'radio_color_side8'},
        {id: 'radio_color_side9'},
        {id: 'radio_color_side10'}
      ],
    }
  }
}
</script>
