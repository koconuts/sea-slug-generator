<template>
  <div>
    <div class="selector-heading-container">
      <h2 class="text selector-heading">頭触手</h2>
    </div>
    <shape-selector
      :shapeSelectorItems="shapeSelectorItemsToushokushu"
      :name="toushokushu"
      @shape="$listeners['toushokushu-shape']"
    ></shape-selector>
    <color-selector
      :colorSelectorItems="colorSelectorItemsToushokushu"
      :name="toushokushuColor"
      @color="$listeners['toushokushu-color']"
    ></color-selector>
    <div class="selector-heading-container">
      <h2 class="text selector-heading">二次鰓</h2>
    </div>
    <shape-selector
      :shapeSelectorItems="shapeSelectorItemsNijiera"
      :name="nijiera"
      @shape="$listeners['nijiera-shape']"
    ></shape-selector>
    <color-selector
      :colorSelectorItems="colorSelectorItemsNijiera"
      :name="nijieraColor"
      @color="$listeners['nijiera-color']"
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
      nijiera: 'nijiera',
      toushokushuColor: 'toushokushuColor',
      nijieraColor: 'nijieraColor',
      shapeSelectorItemsToushokushu: [
        {id: 'shape_toushokushu1', fileName: 'shape_toushokushu_1'},
        {id: 'shape_toushokushu2', fileName: 'shape_toushokushu_2'},
        {id: 'shape_toushokushu3', fileName: 'shape_toushokushu_3'},
        {id: 'shape_toushokushu4', fileName: 'shape_toushokushu_4'}
      ],
      shapeSelectorItemsNijiera: [
        {id: 'shape_nijiera1', fileName: 'shape_nijiera_1'},
        {id: 'shape_nijiera2', fileName: 'shape_nijiera_2'},
        {id: 'shape_nijiera3', fileName: 'shape_nijiera_3'},
        {id: 'shape_nijiera4', fileName: 'shape_nijiera_4'}
      ],
      colorSelectorItemsToushokushu: [
        {id: 'radio_color_toushokushu1', color: {backgroundColor: '#A3A3A3'}},
        {id: 'radio_color_toushokushu2', color: {backgroundColor: '#FFFFFF', boxShadow: '0px 0px 1px inset'}},
        {id: 'radio_color_toushokushu3', color: {backgroundColor: '#F09DF9'}},
        {id: 'radio_color_toushokushu4', color: {backgroundColor: '#F6CD9F'}},
        {id: 'radio_color_toushokushu5', color: {backgroundColor: '#FFFEA5'}},
        {id: 'radio_color_toushokushu6', color: {backgroundColor: '#B1FCA3'}},
        {id: 'radio_color_toushokushu7', color: {backgroundColor: '#B0FCFD'}},
        {id: 'radio_color_toushokushu8', color: {backgroundColor: '#A3CAFA'}},
        {id: 'radio_color_toushokushu9', color: {backgroundColor: '#9998F8'}},
        {id: 'radio_color_toushokushu10', color: {backgroundColor: '#C49BF8'}},
      ],
      colorSelectorItemsNijiera: [
        {id: 'radio_color_nijiera1', color: {backgroundColor: '#A3A3A3'}},
        {id: 'radio_color_nijiera2', color: {backgroundColor: '#FFFFFF', boxShadow: '0px 0px 1px inset'}},
        {id: 'radio_color_nijiera3', color: {backgroundColor: '#F09DF9'}},
        {id: 'radio_color_nijiera4', color: {backgroundColor: '#F6CD9F'}},
        {id: 'radio_color_nijiera5', color: {backgroundColor: '#FFFEA5'}},
        {id: 'radio_color_nijiera6', color: {backgroundColor: '#B1FCA3'}},
        {id: 'radio_color_nijiera7', color: {backgroundColor: '#B0FCFD'}},
        {id: 'radio_color_nijiera8', color: {backgroundColor: '#A3CAFA'}},
        {id: 'radio_color_nijiera9', color: {backgroundColor: '#9998F8'}},
        {id: 'radio_color_nijiera10', color: {backgroundColor: '#C49BF8'}},
      ],
    }
  }
}
</script>
