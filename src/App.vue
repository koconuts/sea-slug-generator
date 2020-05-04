<template>
  <div>
    <header class="header">
      <p class="title">
        <img src="../src/assets/images/title.png">
      </p>
    </header>
    <div class="body">
      <div class="left-container">
        <main-canvas
          :shape="shape"
          :color="color"
          @img-url="getImgUrl"
        ></main-canvas>
        <p class="text pc-right">© 2020 @avocadoneko</p>
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
        <div @click="openModal()" id="complete" class="btn complete-btn">
          <p class="text btn-text">かんせい</p>
        </div>
        <p class="text right">© 2020 @avocadoneko</p>
        <div v-if="showModal" class="overlay">
          <div class="modal">
            <div class="close-btn">
              <i @click="closeModal()" class="fas fa-times fa-3x"></i>
            </div>
            <div class="modal-parent">
              <img :src="imgUrl" class="complete-img">
              <p class="text caution">iPhone の場合は、画像を長押しすると保存ができます。</p>
              <div id="download" class="btn modal-btn">
                <p class="text btn-text">ダウンロード</p>
              </div>
              <div @click="closeModal()" class="btn back-btn modal-btn">
                <p class="text btn-text back-btn-text">もどる</p>
              </div>
            </div>
          </div>
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
    getImgUrl(url) {
      this.imgUrl = url
    },
    openModal() {
      this.showModal = true;
    },
    closeModal() {
      this.showModal = false;
    }
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
        'shape_surface3',
      ],
      color: [
        'radio_color_body9',
        'radio_color_toushokushu5',
        'radio_color_nijiera5',
        'radio_color_surface4',
        'radio_color_side4',
        'radio_color_bg1'
      ],
      imgUrl: '',
      showModal: false,
    }
  }
}
</script>
