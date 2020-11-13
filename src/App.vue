<template id="app">
  <div class="headingWrapper">
    <ImageUpload/>
    <ColorBox :boxColor="colorValue" />
  </div>
  <SelectedImage @current-color="addColorToBox"/>
</template>

<script>

import ImageUpload from "@/components/ImageUpload";
import ColorBox from "@/components/ColorBox";
import SelectedImage from "@/components/SelectedImage";

export default {
  name: 'App',
  components: { ColorBox, ImageUpload, SelectedImage },
  data() {
    return {
      colorValue: null
    }
  },
  methods: {
    addColorToBox(color) {
      this.colorValue = color;
    }
  },
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
.headingWrapper {
  display: flex;
  flex-direction: row;
}
.headingWrapper > * {
  flex: 1;
}
</style>
