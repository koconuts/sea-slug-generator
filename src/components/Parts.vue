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
        <!-- 選択状態 -->
        <li class="item color-item selected"></li>
        <!-- 未選択状態 -->
        <li class="item color-item"></li>
        <li class="item color-item"></li>
        <li class="item color-item"></li>
        <li class="item color-item"></li>
      </ul>
      <ul class="selector color-selector">
        <li class="item color-item"></li>
        <li class="item color-item"></li>
        <li class="item color-item"></li>
        <li class="item color-item"></li>
        <li class="item color-item"></li>
      </ul>
    </div>
    <div class="selector-heading-container">
        <h2 class="text selector-heading">二次鰓</h2>
    </div>
    <div class="container">
      <ul class="selector shape-selector">
        <!-- 選択状態 -->
        <li class="item shape-item selected">
          <img class="shape-item-img" src="../assets/images/parts/slug-parts_1.png">
        </li>
        <!-- 未選択状態 -->
        <li class="item shape-item">
          <img class="shape-item-img" src="../assets/images/parts/slug-parts_1.png">
        </li>
        <li class="item shape-item">
          <img class="shape-item-img" src="../assets/images/parts/slug-parts_1.png">
        </li>
        <li class="item shape-item">
          <img class="shape-item-img" src="../assets/images/parts/slug-parts_1.png">
        </li>
      </ul>
    </div>
    <div class="container">
      <ul class="selector color-selector">
        <!-- 選択状態 -->
        <li class="item color-item selected"></li>
        <!-- 未選択状態 -->
        <li class="item color-item"></li>
        <li class="item color-item"></li>
        <li class="item color-item"></li>
        <li class="item color-item"></li>
      </ul>
      <ul class="selector color-selector">
        <li class="item color-item"></li>
        <li class="item color-item"></li>
        <li class="item color-item"></li>
        <li class="item color-item"></li>
        <li class="item color-item"></li>
      </ul>
    </div>
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
      ]
    }
  }
}
</script>
