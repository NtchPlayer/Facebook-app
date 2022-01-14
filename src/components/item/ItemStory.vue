<template>
  <article class="story-item" :class="{'story-item-add': add}" :style="{ backgroundImage: `url(${img})` }">
    <a href="#">
      <figure v-show="!add">
        <img src="@/assets/user-default.webp" alt="Photo de Profile">
      </figure>
      <h1 v-text="title" />
      <p class="story-item-add-card" v-show="add">
        <span aria-hidden="true" class="fas fa-plus" />
        <span>Créer une story</span>
      </p>
    </a>
  </article>
</template>

<script>
export default {
  name: 'ItemStory',
  props: {
    title: { type: String },
    img: { type: String },
    add: { type: Boolean, default: false }
  }
}
</script>

<style>
.story-item{
  border-radius: 10px;
  background-position: center;
  width: calc(20% - 10px);
}

.story-item a{
  border-radius: 10px;
  backdrop-filter: brightness(70%);
  height: 220px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  line-height: 1.3rem;
  font-size: 0.8rem;
  font-weight: 510;
  padding: 10px;
}

.story-item-add a{
  padding: 0;
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

.story-item .story-item-add-card{
  position: relative;
  background-color: var(--background-color-2);
  padding: 30px 10px 10px 10px;
  text-align: center;
}

.story-item .fa-plus{
  background-color: var(--primary-color);
  position: absolute;
  z-index: 5;
  border: 4px solid var(--background-color-2);
  border-radius: 50%;
  font-size: 1.2rem;
  padding: 10px;
  width: 45px;
  height: 45px;
  display: flex;
  justify-content: center;
  align-items: center;
  left: 50%;
  transform: translateX(-50%) translateY(50%);
  bottom: 100%;
}
</style>
