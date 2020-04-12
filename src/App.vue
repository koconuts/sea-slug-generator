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
              <li class="item part-item selected">
                <h2 class="text part-item-name selected">からだ</h2>
              </li>
              <!-- 未選択状態 -->
              <li class="item part-item">
                <h2 class="text part-item-name">ぱーつ</h2>
              </li>
              <li class="item part-item">
                <h2 class="text part-item-name">もよう</h2>
              </li>
              <li class="item part-item">
                <h2 class="text part-item-name">背景</h2>
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
