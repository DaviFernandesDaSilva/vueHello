<script setup>
const emit = defineEmits();

function showAnt(){
    emit('ant-page');
}
function showProx(){
    emit('prox-page');
}

let texto = "Não obstante, o consenso sobre a necessidade de qualificação é uma das consequências das diretrizes de desenvolvimento para o futuro.";
</script>

<template>
        <div class="container">
        <div class="principal">
            <h1>Fenômeno da Internet!</h1>
            <p>{{ texto }}</p>
        </div>
        <div class="buttons">
            <div class="item">
                    <h3 @click="showAnt">Anterior</h3>
            </div>
            <div class="item">
                    <h3 @click="showProx">Próximo</h3>
            </div>
        </div>
        
    </div>
</template>

<style>

</style>