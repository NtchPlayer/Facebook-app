<template>
  <article class="category-article">
    <a
      href="#"
      :aria-selected="icon === 'fas fa-user'"
      class="categoryArticleItem"
    >
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
.categoryIcon {
  font-size: 30px;
  margin-right: 15px;
  color: var(--primary-color);
}
.categoryText {
  font-size: 1rem;
}
.categoryArticleItem {
  display: flex;
  align-items: center;
  padding: 11px 25px;
}
.categoryArticleItem:hover {
  background-color: var(--background-component);
}
</style>
