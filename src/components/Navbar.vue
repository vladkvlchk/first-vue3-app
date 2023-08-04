<template>
  <div class="navbar">
    <div @click="$router.push('/')">Vue 3</div>
    <div class="navbar__btns">
      <my-button @click="$router.push('/about')">About</my-button>
      <my-button @click="$router.push('/posts')" style="margin-left: 15px">Posts</my-button>
      <my-button @click="$router.push('/store')" style="margin-left: 15px">Store</my-button>
      <my-button @click="$router.push('/composition')" style="margin-left: 15px">Composition API</my-button>
    </div>
  </div>
</template>

<script></script>

<style scoped>
.navbar {
  height: 50px;
  background-color: rgba(0, 128, 128, 0.224);
  box-shadow: 2px 2px 4px gray;
  display: flex;
  align-items: center;
  padding: 0 15px;
}
.navbar__btns {
  margin-left: auto;
}
</style>
