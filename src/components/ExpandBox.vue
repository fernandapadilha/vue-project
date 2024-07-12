<script setup>
import { ref, computed, defineProps } from 'vue';

//const props = defineProps(['title', 'content']);
const props = defineProps({
    title: {
        type: String,
        required:true
    },
    content: {
        type: String,
        default: "Meu valor default de texto para conteúdo."
    },
    qtde: {
        type: Number,
        default: 1
    }
})
const showContent = ref(false);
const textBotao = computed(
    () => showContent.value ? 'Esconder' : 'Mostrar'
)

</script>

<template>

    <div>
        <button @click="showContent = !showContent">{{ textBotao }}</button>
        <div v-if="showContent" class="expand-box">
            <h1>{{ props.title }}</h1>
            <p>{{ props.content }}</p>
            <p>Quantidade: {{ props.qtde }}</p>
        </div>
    </div>

</template>

<style scoped>
    .expand-box {
        height: 100%;
        padding: 20px;
        border: 1px solid black;
        border-radius: 5px;
        box-shadow: 3px 3px 2px 2px gray;
    }
</style>