<template>
  <header>
      <div class="container">
          <div class="logo col-1 p-3">
              <img src="/spotify-logo.png" alt="logo">
          </div>
          <div class="filter-select">
              <select name="genre" id="filter">
                    <option value="genre" disabled selected>Genre</option>
                    <option value="pop">Pop</option>
                    <option value="jazz">Jazz</option>
                    <option value="metal">Metal</option>
                    <option value="rock">Rock</option>
              </select>
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