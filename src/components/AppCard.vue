<template>
  <li class="object_card text-center pd-1">
    <div class="content">
      <h3>{{ cardObject.title }}</h3>
      <h5>{{ cardObject.original_title }}</h5>
      <p>{{ cardObject.original_language }}</p>
      <p>{{ cardObject.vote_average }}</p>
    </div>
  </li>
</template>

<script>
export default {
  name: "AppCard",
  props: {
    cardObject: Object
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