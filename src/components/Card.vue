<script setup>

</script>

<template>
    <div class="card">
        <h3>Instituto Federal Catarinense</h3>
        <slot>
            <h2>Meu nome:</h2>
        </slot>
    </div>
</template>

<style scoped>
    .card {
        height: 200px;
        width: 400px;
        border: 1px solid black;
        border-radius: 20px;
        box-shadow: 2px 2px 3px 3px gray;
        padding: 20px;
    }
</style>