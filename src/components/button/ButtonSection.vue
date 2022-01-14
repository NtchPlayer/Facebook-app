<template>
  <a href="#" class="button-section" :aria-selected="icon === 'fa-home'">
    <span class="fas" :class="icon" />
  </a>
</template>

<script>
export default {
  name: 'ButtonSection',
  props: {
    icon: { type: String, required: true }
  }
}
</script>

<style>
.button-section{
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 1.5rem;
  border-bottom: 5px solid transparent;
  color: var(--grey-color);
  transition-duration: var(--transition-duration);
}

.button-section:hover{
  color: var(--text-color);
}

.button-section[aria-selected]{
  color: var(--primary-color);
  border-color: var(--primary-color);
}
</style>
