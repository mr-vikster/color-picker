<template id="app">
  <div class="wrapper">
    <ImageUpload/>
    <ColorBox/>
  </div>
  <SelectedImage/>
</template>

<script>
import ImageUpload from '@/components/ImageUpload';
import SelectedImage from '@/components/SelectedImage';
import ColorBox from '@/components/ColorBox';

export default {
  name: 'App',
  components: {
    ColorBox,
    SelectedImage,
    ImageUpload,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0;
}
body {
  margin: 0;
  padding: 0;
  overflow: hidden;
}
.wrapper {
  display: flex;
  flex-direction: row;
}
.wrapper > * {
  flex: 1;
}
</style>
