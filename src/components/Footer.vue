<template>
    <div>
        <footer id="footer">
            <p>Make your burguer &copy; 2024</p>
        </footer>
    </div>
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
        justify-content: center;
        bottom: 0;
        width: 100%;
    }
</style>