<template>
  <div class="container">
    <canvas ref="canvas" class="main-img"></canvas>
  </div>
</template>

<script>
export default {
  name: 'MainCanvas',
  props: {
    shape: Array,
    color: Array,
  },
  methods: {
    draw(shape, color) {
      const canvas = this.$refs.canvas
      canvas.height = canvas.width;
      const ctx = canvas.getContext('2d');
      const baseUrl = 'https://sea-slug-generator.s3-ap-northeast-1.amazonaws.com/img/'

      const srcs = [
        `${baseUrl}bg_${color[5].replace('radio_color_bg', '')}.png`,
        `${baseUrl}body_${color[0].replace('radio_color_body', '')}.png`,
        `${baseUrl}nijiera_${shape[1].replace('shape_nijiera', '')}_${color[2].replace('radio_color_nijiera', '')}.png`,
        `${baseUrl}pattern_${shape[2].replace('shape_surface', '')}_${color[3].replace('radio_color_surface', '')}.png`,
        `${baseUrl}toushokushu_${shape[0].replace('shape_toushokushu', '')}_${color[1].replace('radio_color_toushokushu', '')}.png`,
        `${baseUrl}side_${color[4].replace('radio_color_side', '')}.png`,
      ];

      const imgs = [];
      let count = 0;
      for (var index = 0; index < srcs.length; index++) {
        imgs[index] = new Image();
        imgs[index].src = srcs[index];
        imgs[index].onload = () => {
          count++;
          if (count >= srcs.length) {
            for (var i = 0; i < imgs.length; i++) {
              ctx.drawImage(imgs[i], 0, 0, canvas.width, canvas.height);
            }
          }
        }
      }
    },
  },
  mounted() {
    this.draw(this.shape, this.color);
  },
  watch: {
    shape() {
      this.draw(this.shape, this.color);
    },
    color() {
      this.draw(this.shape, this.color);
    },
  },
}
</script>
