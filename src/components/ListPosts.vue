<script>
import axios from "axios";
import CardPost from "./CardPost.vue";

export default {
  name: "ListPosts",
  components: {
    CardPost,
  },
  data() {
    return {
      posts: [],
    };
  },
  created() {
    axios.get("http://127.0.0.1:8000/api/posts").then((response) => {
      this.posts = response.data;
    });
  },
};
</script>

<template>
  <section>
    <div class="container">
      <div class="row">
        <div class="col-md-4" v-for="post in posts">
          <CardPost :data="post" />
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped></style>
