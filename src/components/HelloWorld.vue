<script setup>
import { ref } from 'vue';

const emit = defineEmits();

function show(){
    emit('prox-page');
}

</script>

<template>
    <div class="container">
        <div class="item">
            <h1>Hello World!</h1>
        </div>
        <div class="item">
                <h3 @click="show">Saiba mais</h3>
        </div>
        
    </div>
</template>

<style scoped>

</style>