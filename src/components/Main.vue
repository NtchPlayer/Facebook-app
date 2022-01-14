<template>
  <main>
    <nav class="category">
      <Category
        v-for="(category, i) in CategoriesList"
        :key="i"
        :icon="category.icon"
        :name="category.name"
      />
      <Shortcut
        v-for="(shortcut, i) in ShortcutList"
        :key="i"
        :icon="shortcut.icon"
        :name="shortcut.name"
      />
    </nav>
    <section class="mainContent section-central"></section>
    <aside class="chatList"></aside>
  </main>
</template>

<script>
import Category from "./category/categoryList.vue";
import Shortcut from "./category/shortcutList.vue";

export default {
  name: "Main",
  components: {
    Category,
    Shortcut,
  },
  data() {
    return {
      CategoriesList: [
        { icon: "fa-user-friends", name: "Amis" },
        { icon: "fa-users", name: "groupes" },
        { icon: "fa-store", name: "Marketplace" },
        { icon: "fa-video", name: "Watch" },
        { icon: "fa-history", name: "Souvenirs" },
        { icon: "fa-image", name: "Activité publicitaire récente" },
        { icon: "fa-seedling", name: "centre de climatologie" },
        { icon: "fa-heart", name: "Collecte de Fonds" },
        {
          icon: "fa-hand-holding-heart",
          name: "Covid-19 -  Centre d'information",
        },
      ],
      ShortcutList: [
        { icon: "fa-user-friends", name: "Amis" },
        { icon: "fa-users", name: "groupes" },
        { icon: "fa-store", name: "Marketplace" },
        { icon: "fa-video", name: "Watch" },
        { icon: "fa-history", name: "Souvenirs" },
        { icon: "fa-image", name: "Activité publicitaire récente" },
        { icon: "fa-seedling", name: "centre de climatologie" },
        { icon: "fa-heart", name: "Collecte de Fonds" },
        {
          icon: "fa-hand-holding-heart",
          name: "Covid-19 -  Centre d'information",
        },
      ],
    };
  },
};
</script>

<style>
main {
  display: grid;
  grid-template-columns: 25% 50% 25%;
  color: white;
}
</style>
