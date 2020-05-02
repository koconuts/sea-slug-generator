<template>
  <div>
    <header class="header">
      <h1 class="text title">うみうしジェネレータ</h1>
    </header>
    <div class="body">
      <div class="left-container">
        <main-canvas
          :shape="shape"
          :color="color"
        ></main-canvas>
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
          <whole-body
            v-show="picked === 'radio_whole-body'"
            @body-color="getBodyColor"
          ></whole-body>
          <parts
            v-show="picked === 'radio_parts'"
            @toushokushu-shape="getToushokushuShape"
            @toushokushu-color="getToushokushuColor"
            @nijiera-color="getNijieraColor"
            @nijiera-shape="getNijieraShape"
          ></parts>
          <design
            v-show="picked === 'radio_design'"
            @surface-shape="getSurfaceShape"
            @surface-color="getSurfaceColor"
            @side-color="getSideColor"
          ></design>
          <back-ground
            v-show="picked === 'radio_back-ground'"
            @bg-color="getBgColor"
          ></back-ground>
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
    getToushokushuShape(id) {
      this.$set(this.shape, 0, id);
    },
    getNijieraShape(id) {
      this.$set(this.shape, 1, id);
    },
    getSurfaceShape(id) {
      this.$set(this.shape, 2, id);
    },
    getBodyColor(id) {
      this.$set(this.color, 0, id);
    },
    getToushokushuColor(id) {
      this.$set(this.color, 1, id);
    },
    getNijieraColor(id) {
      this.$set(this.color, 2, id);
    },
    getSurfaceColor(id) {
      this.$set(this.color, 3, id);
    },
    getSideColor(id) {
      this.$set(this.color, 4, id);
    },
    getBgColor(id) {
      this.$set(this.color, 5, id);
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
      ],
      shape: [
        'shape_toushokushu1',
        'shape_nijiera1',
        'shape_surface1',
      ],
      color: [
        'radio_color_body1',
        'radio_color_toushokushu1',
        'radio_color_nijiera1',
        'radio_color_surface1',
        'radio_color_side1',
        'radio_color_bg1'
      ]
    }
  }
}
</script>
