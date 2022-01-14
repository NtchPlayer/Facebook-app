<template>
  <article>
    <a
      href="#"
      class="category-article"
      :aria-selected="icon === 'fas fa-user'"
    >
      <span class="fas" :class="icon" />
      <span v-text="name" />
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
<style></style>
