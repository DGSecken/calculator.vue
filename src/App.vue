<script setup>
import { reactive } from 'vue';
import Form from './components/Form.vue'
import Result from './components/Result.vue'




  const estado = reactive({
    operation: '+',
    num1: '',
    num2: ''
  })


  const resultado = ()=> {
    const {operation} = estado
    switch(operation) {
      case'-':
      return parseFloat(estado.num1) - parseFloat(estado.num2)
      case'*':
      return parseFloat(estado.num1) * parseFloat(estado.num2)
      case'/':
      return parseFloat(estado.num1) / parseFloat(estado.num2)
      default:
      return parseFloat(estado.num1) + parseFloat(estado.num2)
    }
  }
</script>


<template>
<body>
    <div class="container">
      <Form :operacao="evento=> estado.operation = evento.target.value" :num1="evento => estado.num1 = evento.target.value" :num2="evento => estado.num2 = evento.target.value"></Form>
      <Result :num1="estado.num1" :num2="estado.num2" :result="resultado()"/>
    </div>
</body>


</template>