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
        {id: 'radio_color_bg1', color: {backgroundColor: '#ffbcbc'}},
        {id: 'radio_color_bg2', color: {backgroundColor: '#FEFEFE', boxShadow: '0px 0px 1px inset'}},
        {id: 'radio_color_bg3', color: {backgroundColor: '#ffbcdd'}},
        {id: 'radio_color_bg4', color: {backgroundColor: '#ffbcff'}},
        {id: 'radio_color_bg5', color: {backgroundColor: '#ddbcff'}},
        {id: 'radio_color_bg6', color: {backgroundColor: '#bcbcff'}},
        {id: 'radio_color_bg7', color: {backgroundColor: '#bcddff'}},
        {id: 'radio_color_bg8', color: {backgroundColor: '#bcffff'}},
        {id: 'radio_color_bg9', color: {backgroundColor: '#bcffdd'}},
        {id: 'radio_color_bg10', color: {backgroundColor: '#bcffbc'}},
        {id: 'radio_color_bg11', color: {backgroundColor: '#ddffbc'}},
        {id: 'radio_color_bg12', color: {backgroundColor: '#ffffbc'}},
        {id: 'radio_color_bg13', color: {backgroundColor: '#ffddbc'}},
      ],
    }
  },
}
</script>
