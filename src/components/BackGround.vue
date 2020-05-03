<template>
  <div>
    <color-selector
      :colorSelectorItems="colorSelectorItemsBack"
      :name="backColor"
      @color="$listeners['bg-color']"
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
        {id: 'radio_color_bg1', color: {backgroundColor: '#13125D'}},
        {id: 'radio_color_bg2', color: {backgroundColor: '#FEFEFE', boxShadow: '0px 0px 1px inset'}},
      ],
    }
  },
}
</script>
