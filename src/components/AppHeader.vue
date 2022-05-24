<template>
  <div class="container d-flex">
    <label class="form-label"></label>
    <input v-model="searchInput" class="form-control" placeholder="Type to search..." />
    <button type="button" class="btn btn-danger" @click="$emit('userInput', searchInput)">Search</button>
  </div>
</template>

<script>
export default {
  name: "AppHeader",
  data: function () {
    return {
      searchInput: "",
    };
  },
};
</script>

<style lang="scss" scoped>
</style>