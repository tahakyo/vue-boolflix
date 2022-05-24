<template>
  <section>
    <div class="container">
      <h1>Films</h1>
      <ul class="d-flex flex-wrap">
        <Appcard v-for="item in movies" :key="item.id" :cardObject="item" />
      </ul>
      <h1>Series</h1>
      <ul class="d-flex flex-wrap">
        <Appcard v-for="item in series" :key="item.id" :cardObject="item"/>
      </ul>
    </div>
  </section>
</template>

<script>
import Appcard from "./AppCard";

export default {
  name: "AppMain",
  components: {
    Appcard,
  },
  props: {
    movies: Array,
    series: Array,
  }
};
</script>

<style lang="scss" scoped>
</style>