<template>
  <div id="app">
    <Menu/>
    <Landing/>

    <section class="section">
      <div class="section__content">
        <h3>Quem sou eu</h3>
        <p>
          Olá, meu nome é Arthur Marinheiro Vilela, tenho 21 anos e vivo em Ribeirão Pires, São Paulo. Sou um desenvolver web full-stack com 3 anos de experiencia como autonomo para clientes no exterior, trabalhei com o desenvolvimento de APIs REST e aplicações frontend junto com colegas de toda parte do mundo, usando o Inglês para me comunicar. Me formei em 2022 tecnologo em analise e desenvolvimento de sistemas pela FATEC São Caetando do Sul (2018-2021). Com o patrocinio de um de um grande amigo recebi treinamento, em formato de video conferências, especialidado na linguagem Golang, focado no desenvolvimento de micro-serviços da Ardan Labs. Apesar da experiencia a proficiência com Golang, também criei diversas interfaces de usuário com HTML, CSS e Javascript, porém possuo uma afinidade e interesse ao framework Vue e, recentimente, a combinação deste com a linguagem typescript.
        </p>
        <p>
          Gosto de ter uma visão holistica do processo de desenvolvimento de aplicações web, por isso decidi não me especializar em uma etapa especifica. Mesmo que alguns possam ver como uma falha, isto me fornece uma adaptabilidade a qualquer conjunto de tecnologias e frameworks que o trabalho requerir. Acredito também que programadores não devem ser enciclopedias e que a habilidade mais importante de um desenvolvedor é saber usar o Google e Stack Overflow corretamente.
        </p>
        <a href="#">Meu currículo</a>
      </div>      
    </section>

    <section class="section section--dark">
      <div class="section__content">
        <h3>Projetos</h3>
        <p>Alguns projetos que participei ou criei (infelizmente projetos profissionais estam sobre proteção de acordos de confiabilidade):</p>
      </div>
    </section>

    <section class="section">
      <div class="section__content">
        <h3>Tecnologias</h3>
        <p>Tecnologias que eu já utilizei, tanto para trabalho quanto para minha faculdade:</p>
      </div>
    </section>

    <section class="section">
      <div class="section__content">
        <h3>Contato</h3>
        <p>Segue informações de contato:</p>
      </div>
    </section>

    <div></div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Menu from "./components/Menu.vue";
import Landing from "./components/Landing.vue";

@Component({
  components: {
    Menu,
    Landing,
  },
})
export default class App extends Vue {}
</script>

<style lang="scss">
@import "./assets/scss/_colors.scss";

body {
  background-color: $background;
  margin: 0;
  padding: 0;
  font-size: 16px;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: $text-primary;
}

a {
  color: inherit;
}

#app {
  width: 100%;
  min-height: 100vh;  
}

.section {
  width: 100%;
  min-height: 75vh;
  overflow: hidden;

  &--light {
    background-color: $background;
  }

  &--dark {
    background-color: $background-darker;
    // color: white;
  }

  &__content {
    width: 100%;
    max-width: 1020px;
    margin: 10px auto;
  }
}
</style>
