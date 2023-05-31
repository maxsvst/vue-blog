<template>
  <div class="post">
    <div>
      <div><strong>Название</strong> {{ post.title }}</div>
      <div><strong>Описание</strong> {{ post.body }}</div>
    </div>
    <my-button @click="$emit('remove', post)">X</my-button>
  </div>
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style>
.post {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 15px;
  margin: 15px 0 0 15px;
  border: 2px solid orange;
  border-radius: 10px;
}
</style>
