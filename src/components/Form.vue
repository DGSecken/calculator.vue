<script setup>
    const props = defineProps(['operacao', 'num1', 'num2'])
</script>




<template>
        <div class="operation">
            <h1 class="d-flex justify-content-center mt-4">CALCULADORA ARITIMÉTICA C/ VUE.JS</h1>
            <h2 class="d-flex justify-content-center">Selecione a operação para o resultado</h2>

            <div class="d-flex justify-content-center">
                <input class="me-3" @keyup="props.num1" required type="number" placeholder="Insira o número 1"/>
                <input class="me-3" @keyup="props.num2" required type="number" placeholder="Insira o número 2"/>
            
            <select @change="props.operacao">
                <option value="+">Somar</option>
                <option value="-">Subtrair</option>
                <option value="*">Multiplicar</option>
                <option value="/">Dividir</option>
            </select>
        </div>
    </div>
</template>

<style scoped>
    select {
        font-size: 1.8vw;
        color: whitesmoke !important;
        background: #2802ff !important;
    }  
</style>