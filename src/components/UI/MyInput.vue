<template>
  <input :value="modelValue" @input="updateInput" class="input" type="text" />
</template>

<script>
export default {
  name: "my-input",
  props: {
    modelValue: [],
  },
  methods: {
    updateInput(event) {
      this.$emit("update:modelValue", event.target.value);
    },
  },
};
</script>

<style>
.input {
  width: 99%;
  margin: 10px 0 0 15px;
  padding: 5px 0 5px 5px;
  border: 1px solid orange;
  border-radius: 10px;
}
</style>
