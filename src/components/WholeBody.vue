<template>
  <div>
    <color-selector
      :colorSelectorItems="colorSelectorItemsBody"
      :name="bodyColor"
      @color="$listeners['body-color']"
    ></color-selector>
  </div>
</template>

<script>
import ColorSelector from '../components/ColorSelector.vue';

export default {
  name: 'WholeBody',
  components: {
    ColorSelector,
  },
  data() {
    return {
      bodyColor: 'bodyColor',
      colorSelectorItemsBody: [
        {id: 'radio_color_body1', color: {backgroundColor: '#A3A3A3'}},
        {id: 'radio_color_body2', color: {backgroundColor: '#FFFFFF', boxShadow: '0px 0px 1px inset'}},
        {id: 'radio_color_body3', color: {backgroundColor: '#F09DF9'}},
        {id: 'radio_color_body4', color: {backgroundColor: '#F6CD9F'}},
        {id: 'radio_color_body5', color: {backgroundColor: '#FFFEA5'}},
        {id: 'radio_color_body6', color: {backgroundColor: '#B1FCA3'}},
        {id: 'radio_color_body7', color: {backgroundColor: '#B0FCFD'}},
        {id: 'radio_color_body8', color: {backgroundColor: '#A3CAFA'}},
        {id: 'radio_color_body9', color: {backgroundColor: '#9998F8'}},
        {id: 'radio_color_body10', color: {backgroundColor: '#C49BF8'}},
      ],
    }
  },
}
</script>
