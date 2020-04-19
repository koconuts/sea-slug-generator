<template>
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
  </div>
</template>

<script>
export default {
  name: 'ColorSelector',
  components: {
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
        {id: 'radio_color5'},
        {id: 'radio_color6'},
        {id: 'radio_color7'},
        {id: 'radio_color8'},
        {id: 'radio_color9'},
        {id: 'radio_color10'}
      ]
    }
  }
}
</script>

