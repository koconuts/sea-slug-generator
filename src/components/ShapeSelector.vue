<template>
  <div class="container">
    <ul class="selector shape-selector">
      <li class="item shape-item" v-for="(item, key) in shapeSelectorItems" :key="key">
        <input
          class="shape-item-input"
          :id=item.id
          type="radio"
          :name="name"
          :checked=isChecked(key)
        >
        <label
          :for=item.id
          @click="$emit('shape', item.id)"
          class="text shape-item-label"
        >
          <img class="shape-item-img" :src="getSrc(item.fileName)">
        </label>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'ShapeSelector',
  components: {
  },
  props: {
    shapeSelectorItems: Array,
    name: String,
  },
  methods: {
    isChecked(key) {
      return key === 0 ? 'checked' : '';
    },
    getSrc(fileName) {
      return `https://sea-slug-generator.s3-ap-northeast-1.amazonaws.com/img/${fileName}.png`;
    }
  },
}
</script>

