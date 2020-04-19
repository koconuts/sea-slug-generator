<template>
  <div>
    <color-selector
      :colorSelectorItems="colorSelectorItemsBody"
      :name="bodyColor"
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
        {id: 'radio_color_body1'},
        {id: 'radio_color_body2'},
        {id: 'radio_color_body3'},
        {id: 'radio_color_body4'},
        {id: 'radio_color_body5'},
        {id: 'radio_color_body6'},
        {id: 'radio_color_body7'},
        {id: 'radio_color_body8'},
        {id: 'radio_color_body9'},
        {id: 'radio_color_body10'}
      ],
    }
  },
}
</script>
