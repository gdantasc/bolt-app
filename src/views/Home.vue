<template>
  <div class="home">
    <div>
      <h1>Crie eventos na melhor plataforma do mercado</h1>
      <p>
        Aqui na Bolt você cria seus eventos, faz conexões com seu publico,
        realizando encontros e compartilhando amizadas e conhecimentos
      </p>
    </div>
    <div class="circle"></div>
    <div class="circle2"></div>
    <img src="../assets/img_home.svg" alt="imagem" />
    <div class="search">
    <Input />
    <Button buttonName="Pesquisar" class="btn"/>
    </div>
  </div>
</template>

<script>
import Input from "../components/Input.vue"
import Button from "../components/Button.vue"

export default {
  name: "Home",
  components: { Input, Button},
};
</script>

<style scoped>
h1 {
  height: 112px;
  width: 521px;
  font-size: 48px;
  margin: 50px 0 35px 60px;
}
p {
  height: 84px;
  width: 343px;
  font-size: 18px;
  font-weight: 400;
  color: #8b8b8b;
  margin-left: 65px;
}
.circle {
  position: absolute;
  top: 1.5rem;
  right: -2.5rem;
  width: 580px;
  height: 610px;
  border-radius: 50%;
  background: rgba(249, 108, 108, 0.103);
}
.circle2 {
  position: absolute;
  top: 1.5rem;
  right: -2.5rem;
  width: 450px;
  height: 475px;
  border-radius: 50%;
  background: rgba(247, 218, 175, 0.253);
}
img {
  position: absolute;
  top: 7.5rem;
  left: 50%;
}
.search {
  display: flex;
  margin: 150px 60px;
}
.btn {
  margin-left: 30px;
}

</style>
