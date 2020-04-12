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
              <!-- 選択状態 -->
              <li class="item part-item">
                <input
                  id="radio_whole-body"
                  type="radio"
                  name="part-item"
                  checked
                >
                <label for="radio_whole-body" class="text part-item-label selected">からだ</label>
              </li>
              <li class="item part-item">
                <input
                  id="radio_parts"
                  type="radio"
                  name="part-item"
                >
                <label for="radio_parts" class="text part-item-label">ぱーつ</label>
              </li>
              <li class="item part-item">
                <input
                  id="radio_pattren"
                  type="radio"
                  name="part-item"
                >
                <label for="radio_pattren" class="text part-item-label">もよう</label>
              </li>
              <li class="item part-item">
                <input
                  id="radio_back-ground"
                  type="radio"
                  name="part-item"
                >
                <label for="radio_back-ground" class="text part-item-label">背景</label>
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
}
</script>
