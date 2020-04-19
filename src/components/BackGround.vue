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
        {id: 'radio_color_back1', color: {backgroundColor: '#ffbcbc'}},
        {id: 'radio_color_back2', color: {backgroundColor: '#FEFEFE', boxShadow: '0px 0px 1px inset'}},
        {id: 'radio_color_back3', color: {backgroundColor: '#ffbcdd'}},
        {id: 'radio_color_back4', color: {backgroundColor: '#ffbcff'}},
        {id: 'radio_color_back5', color: {backgroundColor: '#ddbcff'}},
        {id: 'radio_color_back6', color: {backgroundColor: '#bcbcff'}},
        {id: 'radio_color_back7', color: {backgroundColor: '#bcddff'}},
        {id: 'radio_color_back8', color: {backgroundColor: '#bcffff'}},
        {id: 'radio_color_back9', color: {backgroundColor: '#bcffdd'}},
        {id: 'radio_color_back10', color: {backgroundColor: '#bcffbc'}},
        {id: 'radio_color_back11', color: {backgroundColor: '#ddffbc'}},
        {id: 'radio_color_back12', color: {backgroundColor: '#ffffbc'}},
        {id: 'radio_color_back13', color: {backgroundColor: '#ffddbc'}},
      ],
    }
  },
}
</script>
