<template>
  <li class="object_card text-center pd-1">
    <div class="content">
      <h3>{{ movie.title }}</h3>
      <h5>{{ movie.original_title }}</h5>
      <p>{{ movie.original_language }}</p>
      <p>{{ movie.vote_average }}</p>
    </div>
  </li>
</template>

<script>
export default {
  name: "AppCard",
  props: {
    movie: Object
  }
};
</script>

<style lang="scss" scoped>
.object_card {
  width: calc(100% / 4 - 10px);
  margin: 5px;
  border: 1px solid white;
}
</style>