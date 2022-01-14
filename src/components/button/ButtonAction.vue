<template>
  <li>
    <button class="button-action">
      <span class="fas" :class="icon"></span>
    </button>
  </li>
</template>

<script>
export default {
  name: 'ButtonAction',
  props: {
    icon: { type: String, required: true }
  }
}
</script>

<style>
.button-action{
  background-color: var(--background-component);
  border-radius: 50px;
  font-size: 1.3rem;
  width: 40px;
  height: 40px;
  margin-left: 10px;
}
</style>
