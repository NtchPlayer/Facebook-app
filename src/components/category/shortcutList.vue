<template>
  <article class="category-article">
    <a
      href="#"
      class="shortcut-article"
      :aria-selected="icon === 'fas fa-user'"
    >
      <span class="fas categoryIcon" :class="icon" />
      <span v-text="name" class="categoryText" />
    </a>
  </article>
</template>

<script>
export default {
  name: "Shortcut",
  props: {
    icon: { type: String, required: true },
    name: { type: String, required: true },
  },
};
</script>
<style></style>
