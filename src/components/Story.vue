<template>
  <section id="container-story">
    <ItemStory
        v-for="(story, i) in storyData"
        :key="i"
        :profile-photo="story.profilePhoto"
        :img="story.img"
        :title="story.title"
    />
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
}
</style>
