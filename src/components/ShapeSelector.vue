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
        <label :for=item.id class="text shape-item-label">
          <img class="shape-item-img" src="../assets/images/parts/slug-parts_1.png">
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
    }
  },
  // data() {
    // return {
    //   shapeSelectorItems: [
    //     {id: 'radio_img1'},
    //     {id: 'radio_img2'},
    //     {id: 'radio_img3'},
    //     {id: 'radio_img4'}
    //   ],
    // }
  // }
}
</script>

