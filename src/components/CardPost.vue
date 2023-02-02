<script>
export default {
  name: "CardPost",
  props: {
    data: Object,
  },
};
</script>

<template>
  <div class="card">
    <img
      v-if="data.image_url"
      :src="data.image_url"
      class="card-img-top"
      :alt="data.title"
    />
    <div class="card-body">
      <h5 class="card-title">{{ data.title }}</h5>
      <p class="card-text">
        {{ data.content }}
      </p>
      <router-link
        :to="{ name: 'single-post', params: { slug: data.slug } }"
        class="btn btn-primary"
        >Info</router-link
      >
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
