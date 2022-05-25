<template>
  <li class="object_card text-center pd-1">
    <div class="path_card">
      <img :src="`https://image.tmdb.org/t/p/w342/${cardObject.poster_path}`" alt="">
    </div>
    <div class="content">
      <h3>{{ cardObject.title ? cardObject.title : cardObject.name }}</h3>
      <h5>
        {{ cardObject.original_title ? cardObject.title : cardObject.name }}
      </h5>
      <img
        v-if="languageIsAvailable"
        :src="require(`../assets/img/${cardObject.original_language}.png`)"
        :alt="cardObject.original_language"
      />
      <p v-else>{{ cardObject.original_language }}</p>
      <p>{{ cardObject.vote_average }}</p>
      <!-- <p >{{ cardObject.overview }}</p> -->
    </div>
  </li>
</template>

<script>
export default {
  name: "AppCard",
  props: {
    cardObject: Object,
  },
  data() {
    return {
      flags: ["en", "fr", "it", "ja", "ru", "de", "ar"],
    };
  },
  computed: {
    languageIsAvailable() {
      return this.flags.includes(this.cardObject.original_language);
    },
  },
};
</script>

<style lang="scss" scoped>
.object_card {
  width: calc(100% / 4 - 10px);
  margin: 5px;
  border: 1px solid white;
  .path_card img {
    width: 100%;
  }

}
</style>