<template>
  <div id="app" class="container">
    <h1>Aula de vue.js</h1>
    <hr>
    <form>
      <div class="form-group">
        <label for="nome">Nome:</label>
        <input type="text" class="form-control" id="nome" aria-describedby="nomeHelp" placeholder="Jose da Silva">
        <small id="nomeHelp" class="form-text text-muted">Como as pessoas chamam você</small>
      </div>
      <div class="form-group">
        <label for="telefone">Telefone:</label>
        <input type="text" class="form-control" id="telefone" placeholder="Password" aria-describedby="telefoneHelp">
        <small id="telefoneHelp" class="form-text text-muted">Como as pessoas entram em contato contigo</small>
      </div>
      <div class="form-group">
        <label for="email">E-mail:</label>
        <CaixaTexto tipo="email" class="form-control" id="email" v-on:clicou="this.minhaFuncao"/>
        <small id="emailHelp" class="form-text text-muted">Como a pessoa te manda mensagem</small>
      </div>
      
      <Botao texto="Clique aqui" classe="btn btn-primary" alerta="Este é um alerta" fundo="red" v-on:clicou="this.minhaFuncao"/>  
  </form>
    
  </div>
</template>

<script>
import Botao from './components/Botao.vue';
import CaixaTexto from './components/CaixaTexto.vue';
export default {
  name: 'app',
  components: {
    Botao,
    CaixaTexto
  }, 
  methods: {
    minhaFuncao: function () {
      alert("Muito bem");
    }
  }
}
</script>

<style lang="scss">
@import '../node_modules/bootstrap/scss/bootstrap.scss';
</style>
