<template>
  <form @submit.prevent>
    <h4>Creating post</h4>
    <my-input v-focus v-model="post.title" placeholder="Title" />
    <my-input v-model="post.body" placeholder="Description" />
    <my-button
      @click="createPost"
      style="align-self: flex-end; margin-top: 15px"
      >Create</my-button
    >
  </form>
</template>

<script>
import MyButton from "./UI/MyButton.vue";

export default {
  components: { MyButton },
  data() {
    return {
      post: {
        title: "",
        body: "",
      },
    };
  },
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit("create", this.post);
      this.post = {
        title: "",
        body: "",
      };
    },
  },
};
</script>

<style scoped>
form {
  display: flex;
  flex-direction: column;
}
</style>
