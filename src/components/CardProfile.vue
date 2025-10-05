<template>
  <article class="card">
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
@import "../styles/tokens.css";
.card {
  padding: 1.5rem;
  width: 340px;
  text-align: center;
  border-radius: var(--radius-md);
  background-color: rgba(255, 255, 255, var(--card-opacity));
  box-shadow: var(--elevation-1);
  backdrop-filter: blur(6px);
  border: 1px solid rgba(0, 0, 0, 0.06);
}
.avatar {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  object-fit: cover;
  margin: 0 auto 1rem;
  border: 3px solid rgba(255, 255, 255, 0.9);
}
.card-title {
  font-family: var(--font-display);
  font-size: var(--h3-size);
  color: var(--color-kelp);
  margin: 0 0 6px;
  font-weight: 600;
}
.card-description {
  margin: 0 0 14px;
  color: rgba(0, 0, 0, 0.65);
  font-size: var(--body-size);
}
.btn-primary {
  background: linear-gradient(90deg, var(--color-kelp), var(--color-willow));
  color: var(--color-platinum);
  border: none;
  padding: 10px 16px;
  border-radius: 999px;
  cursor: pointer;
  font-weight: 600;
}
.btn-primary:focus,
.btn-primary:active {
  outline: var(--focus-outline);
  outline-offset: 3px;
}
@media (max-width: 420px) {
  .card {
    width: 92%;
    padding: 1rem;
  }
  .avatar {
    width: 88px;
    height: 88px;
  }
}
</style>
