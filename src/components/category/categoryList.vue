<template>
  <article class="category-article">
    <a href="#" :aria-selected="icon === 'fas fa-user'">
      <span class="fas categoryIcon" :class="icon" />
      <span v-text="name" class="categoryText" />
    </a>
  </article>
</template>

<script>
export default {
  name: "Category",
  props: {
    icon: { type: String, required: true },
    name: { type: String, required: true },
  },
};
</script>
<style>
.category-article {
  margin: 25px 25px;
}
.categoryIcon {
  font-size: 30px;
  margin-right: 15px;
  color: var(--primary-color);
}
.categoryText {
  font-size: 1rem;
}
</style>
