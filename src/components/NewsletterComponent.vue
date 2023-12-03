<template>
    <div class="newsletter pt-32 pb-32">
    <div class="container">
      <div class="display-flex justify-content-space-between align-items-center">
        <div class="titulo">
          <p>CADASTRE-SE EM NOSSA NEWSLETTER</p>
          <p>e receba novidades e promoções</p>
        </div>
        <div class="form display-flex align-items-center gap-8">
          <input type="text" placeholder="Digite seu nome">
          <input type="email" placeholder="Digite seu email">
          <button>Inscreva-se</button>
        </div>
      </div>
    </div>
  </div>

  <footer class="pt-32 pb-32">
    <div class="container">
      <div class="display-flex justify-content-space-between gap-32">
        <div class="logo">
          <img src="images/loja-rodape.png" alt="">
        </div>
        <div class="sobre">
          <h4>Sobre</h4>
          <p>Este projeto foi desenvolvido por os alunos do 4º perído de Sistemas de Informação na Disciplina de Frameworks Frontend, utilizando Vue.JS 3</p>
        </div>
        <div class="cartoes">
          <h4>Formas de Pagamento</h4>
          <img src="images/formas-cartoes.png">
        </div>
      </div>
    </div>
  </footer>

  <div class="copyright text-align-center pt-16 pb-16">
    <div class="container">
      <small><strong>Desenvolvido por:</strong> Carlos Rangel, Rangel Xavier e Carlos Rangel Xavier - Uninassau - IV Período de Sistemas de Informação</small>
    </div>
  </div>
</template>

<script>
export default {
    name: 'NewsletterComponent'
        
}
</script>

<style lang="scss" scoped>

</style>