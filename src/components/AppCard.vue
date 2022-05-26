<template>
  <li class="object_card text-center pd-1">
    <div class="path_card">
      <img
        v-if="imageFound"
        :src="`https://image.tmdb.org/t/p/w342/${imageFound}`"
        :alt="cardObject.poster_path"
      />
      <img
        class="p-4 mt-5"
        v-else
        src="../assets/img/image-not-found.png"
        alt="image-not-found"
      />
    </div>
    <div class="content">
      <!-- <h3>{{ cardObject.title || cardObject.name }}</h3> with "||= 'or" -->
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
      <p>{{ vote5stars }}</p>
      <p>
        <i
          v-for="n in 5"
          :key="n"
          class="fa-star"
          :class="n <= vote5stars ? 'fas' : 'far'"
        ></i>
      </p>
    </div>
    <div class="overview">
      <p>{{ cardObject.overview }}</p>
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
      flags: ["en", "fr", "it", "ja", "ru", "de", "ar", "es", "pt"],
    };
  },
  computed: {
    languageIsAvailable() {
      return this.flags.includes(this.cardObject.original_language);
    },
    imageFound() {
      return this.cardObject.poster_path;
    },
    vote5stars() {
      return Math.ceil(this.cardObject.vote_average / 2);
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../components/style/common.scss";
.object_card {
  width: calc(100% / 4 - 10px);
  margin: 5px;
  border: 1px solid white;
  .path_card {
    min-height: 500px;
    max-height: 500px;
    img {
      width: 100%;
      overflow: hidden;
      padding: 1rem;
    }
  }
  .content {
    min-height: 300px;
    max-height: 300px;
  }
}
</style>