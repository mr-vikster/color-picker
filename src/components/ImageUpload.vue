<template>
  <div>
    <h2>Upload image to start picking</h2>
    <div class="inputWrapper">
      <input type="file" id="file">
      <label for="file" class="uploadButton">Upload</label>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ImageUpload'
}
</script>

<style scoped>
.inputWrapper {
  display: flex;
  width: 400px;
  margin: 0 auto 25px;
  border: 1px solid black;
}
input {
  flex: 3;
  height: 100%;
  visibility: hidden;
  pointer-events: none;
}
.uploadButton {
  flex: 1;
  height: 100%;
  padding: 10px 20px;
  background: peachpuff;
  font-size: 20px;
  border: none;
  cursor: pointer;
}
.uploadButton:hover {
  opacity: .8;
}
.uploadButton:active {
  opacity: .9;
}
</style>