<template>
  <main>
    <aside class="scrollOverflow">
      <section>
        <nav class="category">
          <Category
            v-for="(category, i) in CategoriesList"
            :key="i"
            :icon="category.icon"
            :name="category.name"
          />
        </nav>
      </section>
      <section>
        <h1 class="categoryTitle">Vos raccourcis</h1>
        <nav>
          <Shortcut
            v-for="(shortcut, i) in ShortcutList"
            :key="i"
            :icon="shortcut.icon"
            :name="shortcut.name"
          />
        </nav>
      </section>
    </aside>
    <section class="mainContent section-central">
      <Story />
      <WhatsUp />
    </section>
    <aside class="chatList"></aside>
  </main>
</template>

<script>
import Category from "./category/categoryList.vue"
import Shortcut from "./category/shortcutList.vue"
import Story from './Story.vue'
import WhatsUp from './mainContent/whatsUp.vue'

export default {
  name: "Main",
  components: {
    Category,
    Shortcut,
    Story,
    WhatsUp
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
        { icon: "fa-seedling", name: "Centre de climatologie" },
        { icon: "fa-heart", name: "Collecte de Fonds" },
        {
          icon: "fa-hand-holding-heart",
          name: "Covid-19 -  Centre d'information",
        }
      ],
      ShortcutList: [
        { icon: "fa-user-friends", name: "Amis" },
        { icon: "fa-users", name: "groupes" },
        { icon: "fa-store", name: "Marketplace" },
        { icon: "fa-video", name: "Watch" },
        { icon: "fa-history", name: "Souvenirs" },
        { icon: "fa-image", name: "Activité publicitaire récente" },
        { icon: "fa-seedling", name: "Centre de climatologie" },
        { icon: "fa-heart", name: "Collecte de Fonds" },
        {
          icon: "fa-hand-holding-heart",
          name: "Covid-19 -  Centre d'information",
        }
      ]
    }
  }
}
</script>

<style>
main {
  display: grid;
  grid-template-columns: 25% 50% 25%;
  color: white;
  margin-top: 20px;
}
.scrollOverflow {
  overflow-y: scroll;
  max-height: calc(100vh - 85px);
  scrollbar-width: none; /* Firefox */
  -ms-overflow-style: none; /* IE 10+ */
}
::-webkit-scrollbar {
  background-color: black;
  width: 5px;
}
::-webkit-scrollbar-thumb {
  background: rgb(2, 0, 36);
  background: linear-gradient(
      180deg,
      rgba(2, 0, 36, 1) 0%,
      rgba(137, 143, 156, 1) 51%,
      rgba(0, 0, 0, 1) 100%
  );
}
.categoryTitle {
  color: var(--grey-color);
  margin: 0 25px;
  font-size: 1.1rem;
  font-weight: 600;
  border-top: 1px solid var(--background-component);
  padding-top: 15px;
}
</style>
