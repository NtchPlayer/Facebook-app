<template>
  <li>
    <button class="button-user">
      <figure>
        <img alt="User Photo" src="@/assets/user-default.webp">
      </figure>
      <p>
        <span class="button-user-firstname">Prénom</span>
        <span class="button-user-name" v-show="name">Nom</span>
      </p>
    </button>
  </li>
</template>

<script>
export default {
  name: 'ButtonUser',
  props:{
    name: { type: Boolean, default: true }
  }
}
</script>

<style>
.button-user{
  display: flex;
  align-items: center;
}

.button-user figure{
  width: 30px;
  height: 30px;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-self: center;
  border-radius: 50px;
  margin-right: 10px;
}

.button-user figure img{
  height: 100%;
}

.button-user p{
  font-weight: 500;
}

.button-user-firstname{
  margin-right: 5px;
}
</style>
