<script>
    import { RouterLink } from 'vue-router';
    export default {
        name: 'HeaderComponent',
        computed: {
            pagina() {
                return this.$route.path
            }
        },
        components: {
            RouterLink
        }
    }
</script>

<template>
    <header class="container">
        <h1>FinanTrack</h1>
        <nav class="nav-home" v-show="pagina==='/'">
            <a href="#features">Features</a>
            <a href="#blog">Blog</a>
            <a href="#contact">Contact</a>
            <router-link to="/login">
                <button class="btnSign">Sign Up</button>
            </router-link>
        </nav>
        <nav v-show="pagina==='/FinanTrack'">

        </nav>
    </header>
</template>

<style scoped>
    @import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap');

    .container {
        display: flex;
        justify-content: space-between;
        padding: 15px 30px;
    }

    h1 {
        margin: 0;
        font-family: "Roboto", sans-serif;
        font-weight: 400;
        font-style: normal;
    }

    a{
        text-decoration: none;
        color: inherit;
        font-family: sans-serif;
    }

    a:hover{
        color: #FFFF99; 
    }

    .nav-home{
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 24em;
    }

    .btnSign{
        height: 40px;
        width: 100px;
        background-color: #DDA0DD ;
        font-size: 16px;
        border: none;
        cursor: pointer;
    }

</style>