<script setup>

</script>

<template>
    <div class="card">

        <div class="header">
            <slot name="header"></slot>
        </div>
        <div class="body">
            <slot>Parceiros da vida</slot>
        </div>
        <div v-if="$slots.footer" class="footer">
            <slot name="footer"></slot>
        </div>
        
    </div>
</template>

<style scoped>
    .card{
        height: 200px;
        width: 400px;
        box-shadow: 2px 2px 3px 3px gray;
        border-radius: 20px;
        padding: 10px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }
    .header, .footer {
        background-color: rgb(253, 204, 67);
        height: 60px;
        border-radius: 10px;
        width: 100%;
    }
</style>