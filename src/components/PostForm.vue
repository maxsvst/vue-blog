<template>
  <form @submit.prevent>
    <my-input
      v-model="post.title"
      type="text"
      placeholder="Добавить название поста"
    />
    <my-input
      v-model="post.body"
      type="text"
      placeholder="Добавить описание поста"
    />
    <my-button class="button" type="submit" @click="createPost"
      >Создать</my-button
    >
  </form>
</template>

<script>
export default {
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

<style>
form {
  display: flex;
  flex-direction: column;
}

.button {
  align-self: flex-start;
}
</style>
