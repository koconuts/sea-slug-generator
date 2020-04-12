<template>
  <div>
    <header class="header">
      <h1 class="title">うみうしジェネレータ</h1>
    </header>
    <div class="body">
      <div class="left-container">
        <div class="container">
          <img class="main-img" src="./assets/images/slug_1.png">
        </div>
      </div>
      <div class="right-container">
        <div class="container">
          <ul class="selector part-selector">
            <!-- 選択状態 -->
            <li class="item part-item selected">
              <h2 class="part-item-name selected">からだ</h2>
            </li>
            <!-- 未選択状態 -->
            <li class="item part-item">
              <h2 class="part-item-name">頭触手</h2>
            </li>
            <li class="item part-item">
              <h2 class="part-item-name">二次鰓</h2>
            </li>
            <li class="item part-item">
              <h2 class="part-item-name">もよう</h2>
            </li>
          </ul>
        </div>
        <div class="container">
          <ul class="selector shape-selector">
            <!-- 選択状態 -->
            <li class="item shape-item selected">
              <img class="shape-item-img" src="./assets/images/parts/slug-parts_1.png">
            </li>
            <!-- 未選択状態 -->
            <li class="item shape-item">
              <img class="shape-item-img" src="./assets/images/parts/slug-parts_1.png">
            </li>
            <li class="item shape-item">
              <img class="shape-item-img" src="./assets/images/parts/slug-parts_1.png">
            </li>
            <li class="item shape-item">
              <img class="shape-item-img" src="./assets/images/parts/slug-parts_1.png">
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
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {
  }
}
</script>
