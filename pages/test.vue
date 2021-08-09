<template>
  <div>
    <div v-for="article in articles" :key="article.title" class="bloc-article">
      <h1>{{ article.title }}</h1>
      <nuxt-content :document="article" />
    </div>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content }) {
    const articles = await $content('articles').fetch()

    return {
      articles
    }
  }
}
</script>

<style>
.bloc-article {
  max-width: 800px;
  margin: 0 auto;
}
</style>
