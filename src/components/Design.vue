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
        {id: 'radio_color_surface1', color: {backgroundColor: '#A3A3A3'}},
        {id: 'radio_color_surface2', color: {backgroundColor: '#FFFFFF', boxShadow: '0px 0px 1px inset'}},
        {id: 'radio_color_surface3', color: {backgroundColor: '#F09DF9'}},
        {id: 'radio_color_surface4', color: {backgroundColor: '#F6CD9F'}},
        {id: 'radio_color_surface5', color: {backgroundColor: '#FFFEA5'}},
        {id: 'radio_color_surface6', color: {backgroundColor: '#B1FCA3'}},
        {id: 'radio_color_surface7', color: {backgroundColor: '#B0FCFD'}},
        {id: 'radio_color_surface8', color: {backgroundColor: '#A3CAFA'}},
        {id: 'radio_color_surface9', color: {backgroundColor: '#9998F8'}},
        {id: 'radio_color_surface10', color: {backgroundColor: '#C49BF8'}},
      ],
      colorSelectorItemsSide: [
        {id: 'radio_color_side1', color: {backgroundColor: '#A3A3A3'}},
        {id: 'radio_color_side2', color: {backgroundColor: '#FFFFFF', boxShadow: '0px 0px 1px inset'}},
        {id: 'radio_color_side3', color: {backgroundColor: '#F09DF9'}},
        {id: 'radio_color_side4', color: {backgroundColor: '#F6CD9F'}},
        {id: 'radio_color_side5', color: {backgroundColor: '#FFFEA5'}},
        {id: 'radio_color_side6', color: {backgroundColor: '#B1FCA3'}},
        {id: 'radio_color_side7', color: {backgroundColor: '#B0FCFD'}},
        {id: 'radio_color_side8', color: {backgroundColor: '#A3CAFA'}},
        {id: 'radio_color_side9', color: {backgroundColor: '#9998F8'}},
        {id: 'radio_color_side10', color: {backgroundColor: '#C49BF8'}},
      ],
    }
  }
}
</script>
