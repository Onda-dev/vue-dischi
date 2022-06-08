<template>
  <header>
      <div class="container">
          <div class="logo col-1 p-3">
              <img src="/spotify-logo.png" alt="logo">
          </div>
      <select-genre/>
      </div>
  </header>
</template>

<script>
import SelectGenre from '../commons/SelectGenre.vue'
export default {
  components: { SelectGenre },
    name: 'HeaderComponent'
}
</script>

<style lang="scss" scoped>
header {
    background-color: #2E3A46;
    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
}
img {
    width: 100%;
}
</style>