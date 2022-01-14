<template>
  <article>
    <h1>Vos raccourcis</h1>
    <a
      href="#"
      class="shortcut-article"
      :aria-selected="icon === 'fas fa-user'"
    >
      <span class="fas" :class="icon" />
      <span v-text="name" />
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
