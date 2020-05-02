<template>
  <div class="container">
    <canvas ref="canvas" class="main-img"></canvas>
    <p>{{ color }}</p>
  </div>
</template>

<script>
export default {
  name: 'MainCanvas',
  props: {
    color: Array,
  },
  methods: {
    draw(color) {
      const canvas = this.$refs.canvas
      canvas.height = canvas.width;
      const ctx = canvas.getContext('2d');

      let srcs = {
        body: `https://sea-slug-generator.s3-ap-northeast-1.amazonaws.com/img/body_${color[0].replace('radio_color_body' , '')}.png`,
        toushokushu: `https://sea-slug-generator.s3-ap-northeast-1.amazonaws.com/img/toushokushu_1_${color[1].replace('radio_color_toushokushu' , '')}.png`,
        nijiera: `https://sea-slug-generator.s3-ap-northeast-1.amazonaws.com/img/nijiera_1_${color[2].replace('radio_color_nijiera' , '')}.png`,
        surface: `https://sea-slug-generator.s3-ap-northeast-1.amazonaws.com/img/pattern_1_${color[3].replace('radio_color_surface' , '')}.png`,
        side: `https://sea-slug-generator.s3-ap-northeast-1.amazonaws.com/img/side_${color[4].replace('radio_color_side' , '')}.png`,
        bg: `https://sea-slug-generator.s3-ap-northeast-1.amazonaws.com/img/bg_${color[5].replace('radio_color_bg' , '')}.png`,
      };

      const bodyImg = new Image();
      bodyImg.onload = function() {
        ctx.drawImage(bodyImg, 0, 0, canvas.width, canvas.height);
      };
      bodyImg.src = srcs.body;

      const toushokushuImg = new Image();
      toushokushuImg.onload = function() {
        ctx.drawImage(toushokushuImg, 0, 0, canvas.width, canvas.height);
      };
      toushokushuImg.src = srcs.toushokushu;

      const nijieraImg = new Image();
      nijieraImg.onload = function() {
        ctx.drawImage(nijieraImg, 0, 0, canvas.width, canvas.height);
      };
      nijieraImg.src = srcs.nijiera;

      const surfaceImg = new Image();
      surfaceImg.onload = function() {
        ctx.drawImage(surfaceImg, 0, 0, canvas.width, canvas.height);
      };
      surfaceImg.src = srcs.surface;

      const sideImg = new Image();
      sideImg.onload = function() {
        ctx.drawImage(sideImg, 0, 0, canvas.width, canvas.height);
      };
      sideImg.src = srcs.side;

      // const bgImg = new Image();
      // bgImg.onload = function() {
      //   ctx.drawImage(bgImg, 0, 0, canvas.width, canvas.height);
      // };
      // bgImg.src = srcs.bg;
    },
  },
  mounted() {
    this.draw(this.color);
  },
  watch: {
    color() {
      this.draw(this.color);
    }
  },
}
</script>
