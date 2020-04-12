<template>
  <div>
    <header class="header">
      <h1 class="title">うみうしジェネレータ</h1>
    </header>
    <div class="container">
      <img class="main-img" src="./assets/images/slug_1.png">
    </div>
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
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {
  }
}
</script>
