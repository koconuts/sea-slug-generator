<template>
  <div>
    <color-selector
      :colorSelectorItems="colorSelectorItemsBack"
      :name="backColor"
    ></color-selector>
  </div>
</template>

<script>
import ColorSelector from '../components/ColorSelector.vue';

export default {
  name: 'BackGround',
  components: {
    ColorSelector,
  },
  data() {
    return {
      backColor: 'backColor',
      colorSelectorItemsBack: [
        {id: 'radio_color_back1'},
        {id: 'radio_color_back2'},
        {id: 'radio_color_back3'},
        {id: 'radio_color_back4'},
        {id: 'radio_color_back5'},
        {id: 'radio_color_back6'},
        {id: 'radio_color_back7'},
        {id: 'radio_color_back8'},
        {id: 'radio_color_back9'},
        {id: 'radio_color_back10'},
        {id: 'radio_color_back11'},
        {id: 'radio_color_back12'},
        {id: 'radio_color_back13'},
      ],
    }
  },
}
</script>
