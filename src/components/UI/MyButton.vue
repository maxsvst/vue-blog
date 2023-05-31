<template>
  <button class="button"><slot></slot></button>
</template>

<script>
export default {
  name: "my-button",
};
</script>

<style>
.button {
  margin: 10px 0 0 15px;
  border: 1px solid orange;
  border-radius: 10px;
  padding: 10px;
  background: none;
}
</style>
