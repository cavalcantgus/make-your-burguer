<template>
    <div id="nav">
        <div id="logo-container">
            <router-link to="/" id="logo-url">
            <img :src="logo" :alt="alt" id="logo">
        </router-link>
        <span id="logo-name">Make Your Burguer</span>
        </div>
        <router-link to="/" id="homelink">Home</router-link> 
        <router-link to="/pedidos" id="orderlink">Pedidos</router-link>
    </div>
</template>

<script>
export default {
    name: 'Navbar',
    props: ['logo', 'alt']
}
</script>

<style scoped>
    #nav {
        background-color: #222;
        border-bottom: 4mm ridge rgb(255, 196, 0);
        padding: 15px 20px;
        display: flex;
        justify-content: flex-end;
        align-items: center;
    }

    #logo-container {
        display: flex;
        align-items: center;
        margin-right: auto;
    }

    #nav #logo-url {
        margin-right: 10px;
    }

    #nav #logo {
        width: 40px;
        height: 40px;
    }

    #logo-name {
        font-size: 20px;
        color: #fff;
        font-weight: bold;
    }

    #nav #homelink, #orderlink {
        color: rgb(255, 196, 0);
        text-decoration: none;
        font-weight: bold;
        border: 3px solid rgb(255, 196, 0);
        background-color: #222;
        border-radius: 10px;
        display: inline-block;
        width: 80px;
        text-align: center;
        padding: 8px ;
        margin: 12px;
        transition: .3s;
    }

    #nav #homelink:hover, #orderlink:hover {
        color: #222;
        font-weight: bold;
        background-color: rgb(255, 196, 0);
    }
</style>