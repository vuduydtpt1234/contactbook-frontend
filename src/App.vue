<script>
import AppHeader from "@/components/AppHeader.vue";

export default {
  components: {
    AppHeader,
  },
};
</script>

<template>
  <AppHeader />

  <div class="container">
    <router-view />
  </div>
</template>

<style>
.page {
  text-align: left;
  max-width: 750px;
  margin: auto;
}
</style>
