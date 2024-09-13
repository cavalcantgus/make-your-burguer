<template>
    <footer id="footer">
        <p>Make your burguer &copy; 2024</p>
    </footer>
</template>

<script>
export default {
    name: 'Footer'
}
</script>

<style scoped>
    #footer {
        height: 200px;
        background-color: #222;
        border-top: 4px solid #111;
        color: rgb(255, 196, 0);
        display: flex;
        align-items: center;
        position: absolute;
        bottom: 0;
        justify-content: center;
        width: 100%;
    }
</style>