<script>
import ListPosts from "../components/ListPosts.vue";

export default {
  name: "HomePage",
  componentes: {
    ListPosts,
  },
  components: { ListPosts },
};
</script>

<template>
  <h1 class="text-center mb-4">Home Page</h1>
  <ListPosts />
</template>

<style lang="scss" scoped></style>
