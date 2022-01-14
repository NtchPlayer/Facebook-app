<template>
  <section class="whatsUpContainer">
    <article class="whatsUpItemContainer">
      <ButtonUser :firstname="false" :name="false" />
      <button class="whatsUpUpperItem">Quoi de neuf, beaugoss ?</button>
    </article>
    <article class="whatsUpItemContainer">
      <a href="#" class="whatsUpBottomItem"
        ><span class="fas fa-video"></span><span>Vidéo en direct</span></a
      >
      <button class="whatsUpBottomItem">
        <span class="fas fa-image"></span><span> Photo/vidéo</span>
      </button>
      <button class="whatsUpBottomItem">
        <span class="fas fa-grin-squint"></span><span>Humeur/Activité</span>
      </button>
    </article>
  </section>
</template>
<script>
import ButtonUser from "../button/ButtonUser.vue";

export default {
  name: "WhatsUp",
  components: {
    ButtonUser,
  },
};
</script>
<style>
.whatsUpContainer {
  height: 123px;
  background-color: var(--grey-color);
  display: flex;
  flex-flow: column nowrap;
  padding: 12px;
}
.whatsUpItemContainer:first-child {
  display: flex;
  align-items: center;
  list-style: none;
  border-bottom: 1px solid var(--background-component);
  padding-bottom: 16px;
  margin-bottom: 10px;
}
.whatsUpItemContainer:last-child {
  width: 100%;
  display: flex;
  align-items: center;
}
.whatsUpBottomItem {
  width: 186px;
  height: 40px;
  padding: 8px;
}

.whatsUpUpperItem {
  width: 510px;
  background-color: red;
  border-radius: 15px;
  height: 40px;
}
.fa-grin-squint {
  color: orange;
}
.fa-image {
  color: green;
}
.fa-vidéo {
  color: red;
}
</style>
