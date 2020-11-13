<template>
  <div class="wrapper">
    <img
      src="https://images.unsplash.com/photo-1605209640818-7ac87291a91f?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1900&q=80"
      alt="uploaded image"
    />
  </div>
</template>

<script>
export default {
  name: "Image"
}
</script>

<style scoped>
.wrapper {
  width: 100vw;
  min-height: 400px;
}
img {
  width: 100%;
  height: 100%;
}
</style>