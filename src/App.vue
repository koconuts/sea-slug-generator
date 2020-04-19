<template>
  <div>
    <header class="header">
      <h1 class="text title">うみうしジェネレータ</h1>
    </header>
    <div class="body">
      <div class="left-container">
        <main-canvas></main-canvas>
      </div>
      <div class="right-container">
        <div class="selectors">
          <div class="container">
            <ul class="selector part-selector">
              <li class="item part-item" v-for="(item, key) in partsSelectorItems" :key="key">
                <input
                  type="radio"
                  name="part-item"
                  :value=item.id
                  :id=item.id
                  :checked=isChecked(key)
                  v-model="picked"
                >
                <label :for=item.id class="text part-item-label">{{ item.label }}</label>
              </li>
            </ul>
          </div>
          <whole-body v-show="picked === 'radio_whole-body'"></whole-body>
          <parts v-show="picked === 'radio_parts'">></parts>
          <design v-show="picked === 'radio_design'"></design>
          <back-ground v-show="picked === 'radio_back-ground'">></back-ground>
        </div>
        <div class="complete-btn">
          <p class="text complete-btn-text">かんせい</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import MainCanvas from './components/MainCanvas.vue'
import WholeBody from './components/WholeBody.vue'
import Parts from './components/Parts.vue'
import Design from './components/Design.vue'
import BackGround from './components/BackGround.vue'

export default {
  name: 'App',
  components: {
    MainCanvas,
    WholeBody,
    Parts,
    Design,
    BackGround
  },
  methods: {
    isChecked(key) {
      return key === 0 ? 'checked' : '';
    },
  },
  data() {
    return {
      picked: 'radio_whole-body',
      partsSelectorItems: [
        {id: 'radio_whole-body', label: 'からだ'},
        {id: 'radio_parts', label: 'ぱーつ'},
        {id: 'radio_design', label: 'もよう'},
        {id: 'radio_back-ground', label: '背景'}
      ]
    }
  }
}
</script>
