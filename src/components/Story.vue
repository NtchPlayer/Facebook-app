<template>
  <section id="container-story">
    <ItemStory :add="true" img="https://picsum.photos/200/300" />
    <ItemStory
        v-for="(story, i) in storyData"
        :key="i"
        :profile-photo="story.profilePhoto"
        :img="story.img"
        :title="story.title"
    />
    <span class="fas fa-arrow-right" />
  </section>
</template>

<script>
import ItemStory from './item/ItemStory.vue'

export default {
  name: 'Story',
  components: {
    ItemStory
  },
  data () {
    return {
      storyData: [
        {
          title: 'Manu Romero Villareal',
          img: 'https://picsum.photos/200/300',
        }, {
          title: 'World Of Clarence',
          img: 'https://picsum.photos/200/300',
        },  {
          title: 'Vincent Lahouze',
          img: 'https://picsum.photos/200/300',
        },  {
          title: 'Paul Silve',
          img: 'https://picsum.photos/200/300',
        }
      ]
    }
  }
}
</script>

<style>
#container-story{
  justify-content: space-between;
  display: flex;
  position: relative;
}

#container-story .fa-arrow-right{
  position: absolute;
  width: 45px;
  height: 45px;
  background-color: var(--background-component);
  font-size: 1.3rem;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
  color: #B0B3B8;
  right: 0;
  transform: translateX(50%) translateY(-50%);
  z-index: 5;
  top: 50%;
}
</style>
