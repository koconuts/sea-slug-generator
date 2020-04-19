<template>
  <div>
    <div class="selector-heading-container">
      <h2 class="text selector-heading">頭触手</h2>
    </div>
    <shape-selector
      :shapeSelectorItems="shapeSelectorItemsToushokushu"
      :name="toushokushu"
    ></shape-selector>
    <color-selector></color-selector>
    <div class="selector-heading-container">
      <h2 class="text selector-heading">二次鰓</h2>
    </div>
    <shape-selector
      :shapeSelectorItems="shapeSelectorItemsNijihai"
      :name="nijihai"
    ></shape-selector>
    <color-selector></color-selector>
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
    }
  }
}
</script>
