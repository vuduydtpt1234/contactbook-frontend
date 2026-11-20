<script>
export default {
  props: {
    modelValue: { type: String, default: "" },
  },

  emits: ["update:modelValue"],
};
</script>

<template>
  <input
    type="text"
    class="form-control"
    placeholder="Tìm kiếm"
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
  />
</template>
