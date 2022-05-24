<template>
  <section>
    <div class="container">
      <ul class="d-flex flex-wrap">
        <Appcard v-for="item in movies" :key="item.id" :movie="item" />
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
    movies: Array
  }
};
</script>

<style lang="scss" scoped>
</style>