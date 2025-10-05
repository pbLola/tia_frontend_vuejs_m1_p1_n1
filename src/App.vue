<template>
  <div class="container app-root">
    <CardProfile />
  </div>
</template>

<script>
import CardProfile from "./components/CardProfile.vue"

export default {
  name: "App",
  components: { CardProfile },
}
</script>
<style>
.app-root {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}
</style>
