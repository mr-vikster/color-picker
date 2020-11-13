<template>
  <div class="imageWrapper">
    <img
      src="https://images.unsplash.com/photo-1605209640818-7ac87291a91f?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1900&q=80"
      alt="uploaded image"
      @click="getPixelValue"
      class="image"
    />
  </div>
</template>

<script>

export default {
  name: "SelectedImage",
  methods: {
    getPixelValue(event) {
      const image = document.querySelector('.image');
      image.crossOrigin = 'Anonymous';
      const canvas = document.createElement('canvas');
      canvas.width = image.clientWidth;
      canvas.height = image.clientHeight;
      canvas.getContext('2d').drawImage(image, 0, 0, image.clientWidth, image.clientHeight)
      const points = canvas
        .getContext('2d')
        .getImageData(event.offsetX, event.offsetY, 1, 1)
        .data;
      localStorage.setItem('current-color', points)
      this.$emit('current-color', points)
    }
  },
}
</script>

<style scoped>
.imageWrapper {
  width: 100vw;
  min-height: 400px;
}
.imageWrapper img {
  width: 100%;
  height: 100%;
  cursor: crosshair;
}
</style>