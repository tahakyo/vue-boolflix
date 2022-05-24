<template>
  <li class="object_card text-center pd-1">
    <div class="content">
      <h3>Titolo</h3>
      <h5>Titolo Originale</h5>
      <p>Lingua</p>
      <p>Voto</p>
    </div>
  </li>
</template>

<script>
export default {
  name: "AppCard",
};
</script>

<style lang="scss" scoped>
  .object_card {
    width: calc(100% / 4 - 10px);
    margin: 5px;
    border: 1px solid white;
    .content {
    }
  }
</style>