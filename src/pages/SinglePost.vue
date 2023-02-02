<script>
import axios from "axios";

export default {
  name: "SinglePost",
  data() {
    return {
      post: null,
    };
  },
  created() {
    axios
      .get(`http://127.0.0.1:8000/api/posts/${this.$route.params.slug}`)
      .then((response) => {
        this.post = response.data;
      })
      .catch(() => {
        this.$router.push({ name: "page-404" });
      });
  },
};
</script>

<template>
  <div>
    <img :src="post.image_url" :alt="post.title" />
    <h1>{{ post.title }}</h1>
    <p>{{ post.content }}</p>
  </div>
</template>

<style lang="scss" scoped></style>
