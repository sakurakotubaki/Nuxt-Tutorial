<template>
  <div>
    <h1>記事一覧</h1>
    <ul>
      <li v-for="post in posts" :key="post.id">
        {{ post.title }}
      </li>
      {{
        posts
      }}
    </ul>
  </div>
</template>

<script>
export default {
  name: 'AsyncComponent',
  data() {
    return {
      posts: [],
    };
  },
  async fetch() {
    const posts = await this.$axios.$get(
      "https://jsonplaceholder.typicode.com/posts/"
    );
    this.posts = posts;
  },
};
</script>
