<template>
  <article>
    <img :src="avatarSrc" alt="Avatar de {{ name }}" class="avatar" />
    <h2 class="card-title">{{ name }}</h2>
    <p class="card-description">{{ description }}</p>
    <button class="btn btn-primary" @click="onConnect">Conectar</button>
  </article>
</template>
<script>
export default {
  name: "CardProfile",
  props: {},
  data() {
    return {
      avatarSrc: "https://i.pravatar.cc/150?img=3",
      name: "Lohanne Castro",
      description: "Desenvolvedora Front-End — TIA Frontend: Vue.js",
    }
  },
  methods: {
    onConnect() {
      alert("Pedido de conexão enviado para ${this.name}")
    },
  },
}
</script>
<style scoped>
.card {
  padding: 12px;
  width: 320px;
  text-align: center;
  border-radius: 12px;
}
.avatar {
  width: 88px;
  height: 88px;
  border-radius: 50%;
  display: block;
  margin: 0 auto 12px;
  object-fit: cover;
}
.card-title {
  margin: 0 0 6px;
  font-weight: 700;
}
.card-description {
  margin: 0 0 12px;
  color: rgba(0, 0, 0, 0.6);
}
</style>
