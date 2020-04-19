<template>
  <div>
    <div class="selector-heading-container">
      <h2 class="text selector-heading">頭触手</h2>
    </div>
    <shape-selector
      :shapeSelectorItems="shapeSelectorItemsToushokushu"
      :name="toushokushu"
    ></shape-selector>
    <color-selector
      :colorSelectorItems="colorSelectorItemsToushokushu"
      :name="toushokushuColor"
    ></color-selector>
    <div class="selector-heading-container">
      <h2 class="text selector-heading">二次鰓</h2>
    </div>
    <shape-selector
      :shapeSelectorItems="shapeSelectorItemsNijihai"
      :name="nijihai"
    ></shape-selector>
    <color-selector
      :colorSelectorItems="colorSelectorItemsNijihai"
      :name="nijihaiColor"
    ></color-selector>
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
  data() {
    return {
      toushokushu: 'toushokushu',
      nijihai: 'nijihai',
      toushokushuColor: 'toushokushuColor',
      nijihaiColor: 'nijihaiColor',
      shapeSelectorItemsToushokushu: [
        {id: 'radio_img1'},
        {id: 'radio_img2'},
        {id: 'radio_img3'},
        {id: 'radio_img4'}
      ],
      shapeSelectorItemsNijihai: [
        {id: 'radio_img5'},
        {id: 'radio_img6'},
        {id: 'radio_img7'},
        {id: 'radio_img8'}
      ],
      colorSelectorItemsToushokushu: [
        {id: 'radio_color1'},
        {id: 'radio_color2'},
        {id: 'radio_color3'},
        {id: 'radio_color4'},
        {id: 'radio_color5'},
        {id: 'radio_color6'},
        {id: 'radio_color7'},
        {id: 'radio_color8'},
        {id: 'radio_color9'},
        {id: 'radio_color10'}
      ],
      colorSelectorItemsNijihai: [
        {id: 'radio_color1'},
        {id: 'radio_color2'},
        {id: 'radio_color3'},
        {id: 'radio_color4'},
        {id: 'radio_color5'},
        {id: 'radio_color6'},
        {id: 'radio_color7'},
        {id: 'radio_color8'},
        {id: 'radio_color9'},
        {id: 'radio_color10'}
      ],
    }
  }
}
</script>
