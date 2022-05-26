<template>
  <div class="container">
    <div class="header_logo text-center p-3">
      <img src="../assets/img/header_logo.png" alt="">
    </div>
    <div class="search_bar d-flex mb-3">
      <label class="form-label"></label>
      <input v-model="searchInput" class="form-control" placeholder="Type to search..." />
      <button type="button" class="btn btn-danger" @click="$emit('userInput', searchInput)">Search</button>
    </div>
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