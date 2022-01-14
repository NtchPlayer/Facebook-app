<template>
  <article class="story-item" :style="{ backgroundImage: `url(${img})` }">
    <a href="#">
      <figure>
        <img src="@/assets/user-default.webp" alt="Photo de Profile">
      </figure>
      <h1 v-text="title" />
    </a>
  </article>
</template>

<script>
export default {
  name: 'ItemStory',
  props: {
    title: { type: String, required: true },
    img: { type: String, required: true }
  }
}
</script>

<style>
.story-item{
  border-radius: 10px;
  background-position: center;
  width: 20%;
}

.story-item a{
  padding: 10px;
  backdrop-filter: brightness(70%);
  height: 220px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.story-item figure{
  width: 40px;
  height: 40px;
  border: 4px solid var(--primary-color);
  overflow: hidden;
  display: flex;
  justify-content: center;
  border-radius: 50px;
}

.story-item figure img{
  height: 100%;
}
</style>
