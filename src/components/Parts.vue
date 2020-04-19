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
        {id: 'radio_img_toushokushu1'},
        {id: 'radio_img_toushokushu2'},
        {id: 'radio_img_toushokushu3'},
        {id: 'radio_img_toushokushu4'}
      ],
      shapeSelectorItemsNijihai: [
        {id: 'radio_img_nijihai5'},
        {id: 'radio_img_nijihai6'},
        {id: 'radio_img_nijihai7'},
        {id: 'radio_img_nijihai8'}
      ],
      colorSelectorItemsToushokushu: [
        {id: 'radio_color_toushokushu1'},
        {id: 'radio_color_toushokushu2'},
        {id: 'radio_color_toushokushu3'},
        {id: 'radio_color_toushokushu4'},
        {id: 'radio_color_toushokushu5'},
        {id: 'radio_color_toushokushu6'},
        {id: 'radio_color_toushokushu7'},
        {id: 'radio_color_toushokushu8'},
        {id: 'radio_color_toushokushu9'},
        {id: 'radio_color_toushokushu10'}
      ],
      colorSelectorItemsNijihai: [
        {id: 'radio_color_nijihai1'},
        {id: 'radio_color_nijihai2'},
        {id: 'radio_color_nijihai3'},
        {id: 'radio_color_nijihai4'},
        {id: 'radio_color_nijihai5'},
        {id: 'radio_color_nijihai6'},
        {id: 'radio_color_nijihai7'},
        {id: 'radio_color_nijihai8'},
        {id: 'radio_color_nijihai9'},
        {id: 'radio_color_nijihai10'}
      ],
    }
  }
}
</script>
