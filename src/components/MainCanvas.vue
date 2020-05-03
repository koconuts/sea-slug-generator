<template>
  <div class="container">
    <canvas ref="canvas" class="main-img" width=600 height=600 style="width:100%;"></canvas>
    <!-- <canvas ref="canvas2" class="main-img" width=600 height=600 style="width:100%;"></canvas> -->
    <!-- <img src="./slug-parts_1.png"> -->
    <!-- <img class="img" width=600 height=600 style="width:100%;"> -->
  </div>
</template>

<script>
// import Img from '../components/slug-parts_1.png'
// import Img from '../components/Parts.vue'
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

      ctx.beginPath()
      ctx.clearRect(0, 0, 200, 200)
      ctx.arc(100, 100, 24, 0, Math.PI * 2)
      ctx.fill()

      const baseUrl = 'https://sea-slug-generator.s3-ap-northeast-1.amazonaws.com/img/'

      // const srcs = [
      //   "./slug-parts_1.png"
      // ]
      const srcs = [
        // `${baseUrl}bg_${color[5].replace('radio_color_bg', '')}.png`,
        `${baseUrl}body_${color[0].replace('radio_color_body', '')}.png`,
        `${baseUrl}nijiera_${shape[1].replace('shape_nijiera', '')}_${color[2].replace('radio_color_nijiera', '')}.png`,
        `${baseUrl}pattern_${shape[2].replace('shape_surface', '')}_${color[3].replace('radio_color_surface', '')}.png`,
        `${baseUrl}toushokushu_${shape[0].replace('shape_toushokushu', '')}_${color[1].replace('radio_color_toushokushu', '')}.png`,
        `${baseUrl}side_${color[4].replace('radio_color_side', '')}.png`,
      ];

      // console.log(srcss);

      const imgs = [];
      let count = 0;
      for (var index = 0; index < srcs.length; index++) {
        imgs[index] = new Image();
        imgs[index].crossOrigin = "";
        imgs[index].src = srcs[index];
        imgs[index].onload = () => {
          count++;
          if (count >= srcs.length) {
            for (var i = 0; i < imgs.length; i++) {
              ctx.drawImage(imgs[i], 0, 0, canvas.width, canvas.height);
              // const blob = new Blob(imgs, {type: 'image/png'});
              // console.log(blob);
              // console.log(URL.createObjectURL(blob));
            }
          }
        }
        // console.log(canvas.toDataURL());
        // imgs[index].src = srcs[index];
      }
      canvas.toBlob(function(blob) {
        var newImg = document.createElement("img"),
            url = URL.createObjectURL(blob);
        console.log(url);
        newImg.src = url;
        document.body.appendChild(newImg);
      });
      // const blob = new Blob(imgs, {type: 'image/png'});
      // console.log(blob);
      console.log(canvas.toDataURL());
      // const canvas2= this.$refs.canvas2;
      // console.log(canvas2);
      // var newImage = ctx.getImageData(0, 0, canvas.width, canvas.height);
      // console.log(newImage);
      // canvas2.getContext('2d').drawImage(canvas, 0, 0);
      // console.log(URL.createObjectURL(blob));
    },
    download() {
      // const canvas = this.$refs.canvas
      // const uri = canvas.toDataURL();
    }
  },
  mounted() {
    this.draw(this.shape, this.color);
    // console.log(this.$refs.canvas.toDataURL());
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
