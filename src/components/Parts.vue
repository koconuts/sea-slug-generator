<template>
  <div>
    <div class="selector-heading-container">
      <h2 class="text selector-heading">頭触手</h2>
    </div>
    <shape-selector></shape-selector>
    <div class="container">
      <ul class="selector color-selector">
        <li class="item color-item" v-for="(item, key) in colorSelectorItems" :key="key">
          <input
            :id=item.id
            type="radio"
            name="color-item"
            :checked=isChecked(key)
          >
          <label :for=item.id class="text color-item-label"></label>
        </li>
      </ul>
      <ul class="selector color-selector">
        <li class="item color-item" v-for="(item, key) in colorSelectorItems2" :key="key">
          <input
            :id=item.id
            type="radio"
            name="color-item"
          >
          <label :for=item.id class="text color-item-label"></label>
        </li>
      </ul>
    </div>
    <!-- <div class="selector-heading-container">
      <h2 class="text selector-heading">二次鰓</h2>
    </div> -->
  </div>
</template>

<script>
import ShapeSelector from '../components/ShapeSelector.vue';

export default {
  name: 'Parts',
  components: {
    ShapeSelector,
  },
  methods: {
    isChecked(key) {
      return key === 0 ? 'checked' : '';
    }
  },
  data() {
    return {
      colorSelectorItems: [
        {id: 'radio_color1'},
        {id: 'radio_color2'},
        {id: 'radio_color3'},
        {id: 'radio_color4'},
        {id: 'radio_color5'}
      ],
      colorSelectorItems2: [
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
