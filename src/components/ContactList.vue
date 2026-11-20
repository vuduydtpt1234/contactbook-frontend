<script>
export default {
  props: {
    contacts: { type: Array, default: () => [] },
    activeIndex: { type: Number, default: -1 },
  },

  emits: ["update:activeIndex"],
};
</script>

<template>
  <ul class="list-group">
    <li
      class="list-group-item"
      :class="{ active: index === activeIndex }"
      v-for="(contact, index) in contacts"
      :key="contact._id"
      @click="$emit('update:activeIndex', index)"
    >
      {{ contact.name }}
    </li>
  </ul>
</template>
