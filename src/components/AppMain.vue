<script>
import ListPosts from "./ListPosts.vue";
export default {
  name: "AppMain",
  components: { ListPosts },
};
</script>

<template>
  <main>
    <router-view></router-view>
  </main>
</template>

<style lang="scss" scoped></style>
