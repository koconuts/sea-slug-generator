<template>
  <div>
    <header class="header">
      <h1 class="text title">うみうしジェネレータ</h1>
    </header>
    <div class="body">
      <div class="left-container">
        <div class="container">
          <img class="main-img" src="./assets/images/slug_1.png">
        </div>
      </div>
      <div class="right-container">
        <div class="selectors">
          <div class="container">
            <ul class="selector part-selector">
              <li class="item part-item" v-for="(item, key) in partsSelectorItems" :key="key">
                <input
                  :id=item.id
                  type="radio"
                  name="part-item"
                  checked
                >
                <label :for=item.id class="text part-item-label">{{ item.label }}</label>
              </li>
            </ul>
          </div>
          <whole-body></whole-body>
          <parts></parts>
          <!-- <pattern></pattern>
          <back-ground></back-ground> -->
        </div>
        <div class="complete-btn">
          <p class="text complete-btn-text">かんせい</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import WholeBody from './components/WholeBody.vue'
import Parts from './components/Parts.vue'
// import Pattern from './components/Pattern.vue'
// import BackGround from './components/BackGround.vue'

export default {
  name: 'App',
  components: {
    WholeBody,
    Parts,
    // Pattern,
    // BackGround
  },
  data() {
    return {
      partsSelectorItems: [
        {id: 'radio_whole-body', label: 'からだ'},
        {id: 'radio_parts', label: 'ぱーつ'},
        {id: 'radio_pattern', label: 'もよう'},
        {id: 'radio_back-ground', label: '背景'}
      ]
    }
  }
}
</script>
