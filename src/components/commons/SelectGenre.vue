<template>
    <div class="filter-select">
        <select name="genre" id="filter" v-model="filterGenre" @change="$emit('filter', filterGenre)">
            <option value="genre" disabled selected>Select genre</option>
            <option value="pop">Pop</option>
            <option value="jazz">Jazz</option>
            <option value="metal">Metal</option>
            <option value="rock">Rock</option>
        </select>
    </div>
</template>

<script>
export default {
    name: 'SelectGenre',
    data() {
        return {
            filterGenre: ''
        }
    }
}
</script>

<style lang="scss" scoped>

</style>