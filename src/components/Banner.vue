<template>
    <div id="main-banner">
        <h1>Make your burger</h1>
    </div>
</template>

<script>
export default {
    name: 'Banner'
}
</script>

<style scoped>
    #main-banner {
        background-image: url('/public/img/burger.jpg');
        background-position: 0 -250px;
        background-size: cover;
        height: 90vh;
        display: flex;
        align-items: center;
        justify-content: flex-start; /* Center horizontally */
        position: relative;
        overflow: hidden; /* Ensure no overflow */
    }

    #main-banner h1 {
        color: #FFF;
        text-align: center;
        font-size: 60px;
        padding: 20px 40px;
        position: relative;
        z-index: 1; 
    }

    #main-banner h1::before {
        content: 'Make your burger'; 
        position: absolute;
        top: 70px;
        left: 0;
        z-index: -1; 
        color: transparent;
        -webkit-text-stroke-width: 2px;
        -webkit-text-stroke-color: rgb(211, 169, 30);;
        font-size: 60px;
        width: 100%; 
        text-align: center; 
    }

    #main-banner h1::after {
        content: 'Make your burger'; 
        position: absolute;
        bottom: 70px;
        left: 0;
        z-index: -1; 
        color: transparent;
        -webkit-text-stroke-width: 2px;
        -webkit-text-stroke-color: rgb(211, 169, 30);;
        font-size: 60px;
        width: 100%; 
        text-align: center; 
    }
</style>