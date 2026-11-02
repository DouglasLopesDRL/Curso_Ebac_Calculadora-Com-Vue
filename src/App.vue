<script setup>
  import {reactive} from 'vue';
  import Cabecalho from './components/Cabecalho.vue';
  import Formulario from './components/Formulario.vue';
  import Resultado from './components/Resultado.vue';

  const estado = reactive({
    operacao: 'soma',
    valor1: 0,
    valor2: 0,
    resultado: 0,
  });

  const calcular = () => {
    // Lógica de cálculo será implementada aqui
    const {operacao} = estado;
    switch(operacao){
      case 'soma':
        return estado.resultado = estado.valor1 + estado.valor2;
      case 'subtracao':
        return estado.resultado = estado.valor1 - estado.valor2;
      case 'multiplicacao':
        return estado.resultado = estado.valor1 * estado.valor2;
      case 'divisao':
        return estado.resultado = estado.valor1 / estado.valor2;
      default:
        return 0;
    }
  };

  const getResultado = () => {
    calcular();
    return estado.resultado;
  };

</script>

<template>
  <div class="container">
    <Cabecalho />
    <Formulario :operacao="estado.operacao" :altera-operacao="evento => estado.operacao = evento.target.value" :valor1="estado.valor1" :altera-valor1="evento => estado.valor1 = Number(evento.target.value)" :valor2="estado.valor2" :altera-valor2="evento => estado.valor2 = Number(evento.target.value)" />
    <Resultado :resultado="getResultado()" />
  </div>
</template>

<style scoped>

</style>
