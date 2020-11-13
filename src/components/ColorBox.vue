<template>
  <div class="colorBoxContainer">
    <div class="colorBox">
<!--      {{boxColor}}-->
<!--      {{ hexValue }}-->
      {{ rgbValue }}
    </div>
  </div>
</template>

<script>

export default {
  name: "ColorBox",
  props: ['boxColor'],
  data() {
    return {
      hexValue: null,
      rgbValue: `R:${this.boxColor[0]},G:${this.boxColor[1]},B:${this.boxColor[2]}`
    }
  },
  methods() {
    return {
      componentToHex(color) {
        const hex = color.toString(16);
        return hex.length === 1 ? `0${hex}` : hex
      },
      rgbToHex(r, g, b) {
        this.data().hexValue = "#" + ((1 << 24) + (r << 16) + (g << 8) + b).toString(16).slice(1);
      },
    }
  },
  computed() {
    console.log(this.boxColor)
  }
}
</script>

<style scoped>
.colorBoxContainer {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.colorBox {
  padding: 15px;
  border: 1px solid #666;
}
</style>