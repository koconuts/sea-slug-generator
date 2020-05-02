<template>
  <div class="container">
    <ul class="selector color-selector">
      <li class="item color-item" v-for="(item, key) in colorSelectorItems" :key="key">
        <input
          class="color-item-input"
          type="radio"
          :id=item.id
          :name="name"
          :checked=isChecked(key)
        >
        <label
          class="text color-item-label"
          :for=item.id
          :style="item.color"
          @click="$emit('color', item.id)"
        ></label>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'ColorSelector',
  components: {
  },
  props: {
    colorSelectorItems: Array,
    name: String,
  },
  methods: {
    isChecked(key) {
      return key === 0 ? 'checked' : '';
    }
  },
}
</script>

