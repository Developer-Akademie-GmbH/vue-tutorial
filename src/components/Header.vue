<template>
    <header>
        <input placeholder="Suche...">
    </header>
</template>

<script>
    export default {
        name: 'Header',
    }
</script>

<style scoped>
header {
    background-color: #F4BC39;
    height: 120px;
    padding: 16px;
    display: flex;
    align-items: flex-end;
    border-bottom-left-radius: 8px;
    border-bottom-right-radius: 8px;
}
</style>