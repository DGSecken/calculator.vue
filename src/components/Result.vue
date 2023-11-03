<script setup>
    const props = defineProps(['num1', 'num2', 'result'])
</script>




<template>
    <span v-if="props.num1 && props.num2 !=''"><h2 class="d-flex justify-content-center">Resultado: {{ props.result }}</h2></span>
    <span v-else-if="props.num1 || props.num2 === ''"><h2 class="d-flex justify-content-center mt-4"><b>Digite os dois números</b></h2></span>
</template>