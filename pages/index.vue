<template>
  <div>
    <h1>{{ article.title }}</h1>
    <nuxt-content :document="article" />
  </div>
</template>

<script>
export default {
  async asyncData ({ $content }) {
    const article = await $content('articles/mon-premier-article').fetch()

    return {
      article
    }
  }
}
</script>
