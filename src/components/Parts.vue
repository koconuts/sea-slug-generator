<template>
  <div>
    <div class="selector-heading-container">
      <h2 class="text selector-heading">頭触手</h2>
    </div>
    <div class="container">
      <!-- TODO: コンポーネント化 -->
      <ul class="selector shape-selector">
        <li class="item shape-item" v-for="(item, key) in shapeSelectorItems" :key="key">
          <input
            :id=item.id
            type="radio"
            name="shape-item"
            checked
          >
          <label :for=item.id class="text shape-item-label">
            <img class="shape-item-img" src="../assets/images/parts/slug-parts_1.png">
          </label>
        </li>
      </ul>
    </div>
    <div class="container">
      <ul class="selector color-selector">
        <li class="item color-item" v-for="(item, key) in colorSelectorItems" :key="key">
          <input
            :id=item.id
            type="radio"
            name="color-item"
            checked
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
            checked
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
export default {
  name: 'Parts',
  components: {
  },
  data() {
    return {
      shapeSelectorItems: [
        {id: 'radio_img1'},
        {id: 'radio_img2'},
        {id: 'radio_img3'},
        {id: 'radio_img4'}
      ],
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
