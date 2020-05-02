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
      const baseUrl = 'https://sea-slug-generator.s3-ap-northeast-1.amazonaws.com/img/'

      const srcs = [
        `${baseUrl}bg_${color[5].replace('radio_color_bg', '')}.png`,
        `${baseUrl}body_${color[0].replace('radio_color_body', '')}.png`,
        `${baseUrl}toushokushu_1_${color[1].replace('radio_color_toushokushu', '')}.png`,
        `${baseUrl}nijiera_1_${color[2].replace('radio_color_nijiera', '')}.png`,
        `${baseUrl}pattern_1_${color[3].replace('radio_color_surface', '')}.png`,
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
    this.draw(this.color);
  },
  watch: {
    color() {
      this.draw(this.color);
    }
  },
}
</script>
