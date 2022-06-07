<template>
  <header>
      <div class="container">
          <div class="logo col-1 p-3">
              <img src="/spotify-logo.png" alt="logo">
          </div>
      </div>
  </header>
</template>

<script>
export default {
    name: 'HeaderComponent'
}
</script>

<style lang="scss" scoped>
header {
    background-color: #2E3A46;
}
img {
    width: 100%;
}
</style>