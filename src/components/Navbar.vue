<template>
    <div id="nav">
        <router-link to="/" id="logo-url">
            <img :src="logo" :alt="alt" id="logo">
        </router-link>
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
        border-bottom: 4px solid #111;
        padding: 15px 20px;
        display: flex;
        justify-content: flex-end;
        align-items: center;
    }

    #nav #logo-url {
        margin: auto;
        margin-left: 0;
    }

    #nav #logo {
        width: 40px;
        height: 40px;
    }

    #nav #homelink, #orderlink {
        color: #2c2828;
        text-decoration: none;
        background-color: rgb(255, 196, 0);
        border-radius: 10px;
        display: inline-block;
        width: 80px;
        text-align: center;
        padding: 10px;
        margin: 12px;
        transition: .3s;
    }

    #nav #homelink:hover, #orderlink:hover {
        background-color: blanchedalmond;
    }
</style>