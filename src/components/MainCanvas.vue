<template>
  <div class="container">
    <canvas ref="canvas" class="main-img"></canvas>
  </div>
</template>

<script>
export default {
  name: 'MainCanvas',
  methods: {
    draw() {
      const canvas = this.$refs.canvas
      canvas.height = canvas.width;
      const ctx = canvas.getContext('2d');
      const img = new Image();
      img.onload = function() {
        ctx.drawImage(img, 0, 0, canvas.width, canvas.height);
      };
      img.src = "https://sea-slug-generator.s3-ap-northeast-1.amazonaws.com/img/slug_1.b0481609.png";
    },
  },
  mounted() {
    this.draw();
  }
}
</script>
