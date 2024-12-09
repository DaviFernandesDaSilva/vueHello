<script setup>
const emit = defineEmits();

function showAnt(){
    emit('ant-page');
}
function showProx(){
    emit('prox-page');
}

let texto = "A certificação de metodologias que nos auxiliam a lidar com a adoção de políticas descentralizadoras auxilia a preparação e a composição dos modos de operação convencionais.";
</script>

<template>
        <div class="container">
        <div class="principal">
            <h1>Avanço tecnológico!</h1>
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