<template>
  <div class="album-grid">
      <div class="row">
          <div class="col-12 col-sm-6 col-lg">a</div>
          <div class="col">b</div>
          <div class="col">c</div>
          <div class="col">d</div>
          <div class="col">e</div>
      </div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
    name: 'SectionAlbum',
    data() {
        return {
            albums: [],
        };
    },
    created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
            this.albums = response.data;
            console.log(response.data);
        })
        .catch((error) => {
            console.log(error);
        })
    }
}
</script>

<style lang="scss" scoped>

</style>