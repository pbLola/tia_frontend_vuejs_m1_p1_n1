<template>
  <div class="container app-root">
    <cardProfile />
  </div>
</template>

<script>
import CardProfile from "./components/CardProfile.vue"

export default {
  name: "App",
  components: { cardProfile },
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
